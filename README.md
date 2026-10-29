**Face Recognition-Based Attendance System**

**Overview**

This project implements a face recognition-based attendance system using OpenCV, YuNet, and SFace. It detects faces in images, recognizes individuals by comparing facial feature embeddings, and generates an attendance report in CSV format.

**Features**

- **Face Detection:** Uses YuNet to detect faces and facial landmarks.
- **Face Recognition:** Uses SFace to extract facial embeddings and identify individuals.
- **Similarity Matching:** Applies cosine similarity to compare detected faces with known reference faces.
- **Unknown Face Handling:** Labels faces as `UNKNOWN` when the similarity score is below the configured threshold.
- **Model Evaluation:** Tests recognition performance using separate evaluation and test datasets.
- **Attendance Generation:** Records recognized individuals with their image name, date, time, similarity score, and attendance status.
- **CSV Export:** Saves the attendance report as `attendance.csv`.

**Workflow**

<img width="567" height="721" alt="Screenshot from 2026-10-26 11-07-41" src="https://github.com/user-attachments/assets/390e85df-6a5a-40c4-9f63-71c23918c7d1" />

**Technologies Used**

- Python
- OpenCV
- NumPy
- Pandas
- YuNet face detector
- SFace face recognizer
- Jupyter Notebook

**Attendance Output**

The generated `attendance.csv` file contains the following columns:

| Column | Description |
|---|---|
| Image | Name of the processed image |
| Name | Recognized person's identity |
| Date | Date of processing |
| Time | Time of processing |
| Similarity | Cosine similarity score |
| Status | Attendance status (`Present`) |

Only the highest-similarity match for each recognized person is retained in the final attendance sheet.

**Privacy and Responsible Use**

Used publicly available image dataset from Kaggle. Follow the dataset's license, terms of use, and any applicable restrictions. Do not upload additional private face images, facial embeddings, or personal attendance records to a public repository.


