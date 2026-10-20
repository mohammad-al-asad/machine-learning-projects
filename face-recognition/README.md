# Face Recognition

Recognizes a known person in a new photo by comparing face embeddings.

**Notebook:** [face_recognition.ipynb](face_recognition.ipynb)

## How it works

1. **Encode:** the [`face_recognition`](https://github.com/ageitgey/face_recognition) library detects the face in an image and turns it into a 128-dimensional embedding (a vector that describes the face).
2. **Register:** the embedding of a reference photo ([reference_face.png](reference_face.png)) is stored with the person's name.
3. **Recognize:** for a new photo, the notebook computes the Euclidean distance between its embedding and each known embedding. If the closest distance is below **0.6**, the face is identified; otherwise it is reported as "Unknown". If no face is detected, it says so.

## Result

Given a different photo of the same person ([test_face.jpg](test_face.jpg)), the notebook correctly returns `Welcome Asad`.

## Tech stack

Python, face_recognition (dlib), NumPy, OpenCV
