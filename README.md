# Facial-Emotion-Recognition-using-OpenCV-and-Deepface
This project implements real-time facial emotion detection using the `deepface` library and OpenCV. It captures video from the webcam, detects faces, and predicts the emotions associated with each face. The emotion labels are displayed on the frames in real-time.


## Dependencies

- [deepface](https://github.com/serengil/deepface): A deep learning facial analysis library that provides pre-trained models for facial emotion detection. It relies on TensorFlow for the underlying deep learning operations.
- [OpenCV](https://opencv.org/): An open-source computer vision library used for image and video processing.



## Approach

1. Import the necessary libraries: `cv2` for video capture and image processing, and `deepface` for the emotion detection model.

2. Load the Haar cascade classifier XML file for face detection using `cv2.CascadeClassifier()`.

3. Start capturing video from the default webcam using `cv2.VideoCapture()`.

4. Enter a continuous loop to process each frame of the captured video.

5. Convert each frame to grayscale using `cv2.cvtColor()`.

6. Detect faces in the grayscale frame using `face_cascade.detectMultiScale()`.

7. For each detected face, extract the face ROI (Region of Interest).

8. Preprocess the face image for emotion detection using the `deepface` library's built-in preprocessing function.

9. Make predictions for the emotions using the pre-trained emotion detection model provided by the `deepface` library.

10. Retrieve the index of the predicted emotion and map it to the corresponding emotion label.

11. Draw a rectangle around the detected face and label it with the predicted emotion using `cv2.rectangle()` and `cv2.putText()`.

12. Display the resulting frame with the labeled emotion using `cv2.imshow()`.

13. If the 'q' key is pressed, exit the loop.

14. Release the video capture and close all windows using `cap.release()` and `cv2.destroyAllWindows()`.





