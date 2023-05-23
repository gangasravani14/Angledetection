import cv2
import math

# Set up video capture from default camera
cap = cv2.VideoCapture(0)

# Define mouse click callback function
dots_list = []

def dots_of_mouse(mouse_click, x_cor, y_cor, flag_var, parameters):
    if mouse_click == cv2.EVENT_LBUTTONDOWN:
        size_of_dot = len(dots_list)
        if size_of_dot != 0 and size_of_dot % 3 != 0:
            cv2.arrowedLine(frame, tuple(dots_list[round((size_of_dot-1)/3)*3]), (x_cor,y_cor), (0,0,255), 2)
        cv2.circle(frame, (x_cor,y_cor), 5, (0,0,255), cv2.FILLED)
        dots_list.append([x_cor,y_cor])

# Define function to find the gradient between two points
def finding_gradient(dot1, dot2):
    return (dot2[1]-dot1[1]) / (dot2[0]-dot1[0])

# Define function to evaluate the angle between the two objects
def evaluate_angle(dots_list):
    dot1, dot2, dot3 = dots_list[-3:]
    m1 = finding_gradient(dot1, dot2)
    m2 = finding_gradient(dot1, dot3)
    angleR = math.atan((m2-m1) / (1+(m2*m1)))
    angleD = round(math.degrees(angleR))
    cv2.putText(frame, str(angleD), (dot1[0]-40, dot1[1]-20), cv2.FONT_HERSHEY_COMPLEX, 1.5, (0,0,255), 2)

# Start the video capture loop
while True:
    ret, frame = cap.read()
    if not ret:
        break

    # Convert the frame to grayscale
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

    # Apply Canny edge detection
    edges = cv2.Canny(gray, 50, 150, apertureSize=3)

    # Find the contours of the objects
    contours, _ = cv2.findContours(edges, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)

    # Sort contours by size and select the two largest contours
    contours = sorted(contours, key=cv2.contourArea, reverse=True)[:2]

    # Draw contours on the frame
    cv2.drawContours(frame, contours, -1, (0, 255, 0), 3)

    # Set mouse callback function for the frame
    cv2.namedWindow('Camera Feed')
    cv2.setMouseCallback('Camera Feed', dots_of_mouse)

    # Evaluate the angle if three points have been selected
    if len(dots_list) % 3 == 0 and len(dots_list) !=0:
        evaluate_angle(dots_list)

    # Display the frame
    cv2.imshow('Camera Feed', frame)

    # Exit the loop if 'q' is pressed
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Release the video capture object and close all windows
cap.release()
cv2.destroyAllWindows()