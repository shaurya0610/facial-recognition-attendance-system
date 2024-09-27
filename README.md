# **Face Recognition Attendance System**

This project is a Flask-based web application that uses face recognition technology to automate the process of attendance marking. The system captures faces using a webcam, identifies the person using a trained machine learning model, and logs attendance in real time.

## **Features**
- Real-time face detection using OpenCV and webcam integration.
- Face recognition using a K-Nearest Neighbors (KNN) model trained on user images.
- Automated attendance logging in CSV format with timestamps.
- Web interface to add and manage users, view attendance, and delete users.
- Dynamic web pages created using Jinja templating in Flask.

## **Tech Stack**
- **Backend**: Python, Flask, OpenCV, scikit-learn, joblib
- **Frontend**: HTML (Jinja Templates), CSS (if styling is added)
- **Database**: CSV files (for attendance tracking)
- **Machine Learning**: K-Nearest Neighbors (KNN) for face recognition
- **Image Processing**: Haar Cascade Classifier for face detection (OpenCV)

## **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/face-recognition-attendance-system.git
   cd face-recognition-attendance-system
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the Haar Cascade for face detection:
   ```bash
   wget https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml
   ```

4. Run the application:
   ```bash
   python app.py
   ```

## **Usage**

1. Navigate to `http://127.0.0.1:5000/` in your browser.
2. To add a new user, go to the **Add User** page and capture face images.
3. The model will retrain automatically once new faces are added.
4. Start the attendance system by clicking **Start Attendance**, and it will recognize users and log their attendance.
5. View attendance records on the home page and manage users via the **List Users** page.

## **Project Structure**
```
face-recognition-attendance-system/
│
├── Attendance/                     # Folder to store attendance logs
├── static/
│   ├── faces/                      # Folder to store user face images
│   └── face_recognition_model.pkl   # Trained face recognition model
├── templates/
│   ├── home.html                   # Main HTML page for attendance display
│   ├── listusers.html              # HTML page for listing users
│   └── adduser.html                # HTML page for adding new users
├── app.py                          # Flask app with face recognition logic
├── requirements.txt                # Python dependencies
└── README.md                       # Project documentation
```
