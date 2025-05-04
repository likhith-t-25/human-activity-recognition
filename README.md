
# 📊 Sensor Activity Classifier (Accelerometer + Gyroscope)

This project is a **machine learning-based Human Activity Recognition (HAR) tool** that classifies human activities based on sensor data from accelerometer and gyroscope readings. It features a **Gradio-based user interface** for easy CSV uploads and visual output.

## 🔍 Features
- Upload your own sensor CSV data (with activity labels).
- Automatically detects and handles missing values.
- Uses all numeric columns (including both accelerometer and gyroscope data) for feature extraction.
- Trains a **Random Forest classifier** to classify activities.
- Displays:
  - **Classification Report** with accuracy and metrics.
  - **Confusion Matrix** heatmap.
  - **Feature Importance** plot.

## 🧠 Technologies Used
- Python 3
- Pandas & NumPy (data processing)
- scikit-learn (machine learning)
- Matplotlib & Seaborn (visualization)
- Gradio (user interface)
- PIL (image handling)

## 📁 Sample Input Format
The uploaded CSV file should contain:
- **Numeric columns** for sensor data (e.g., `Accel_X`, `Gyro_Y`, etc.)
- One **label column** (named like `Activity`, `activity`, or `Label`) indicating the activity.

Example:

```csv
Accel_X,Accel_Y,Accel_Z,Gyro_X,Gyro_Y,Gyro_Z,Activity
0.01,-0.02,9.81,0.05,0.01,-0.03,Walking
0.04,0.02,9.78,0.07,0.02,-0.01,Running
...
```

## 🚀 How to Use

1. **Install dependencies**:

```bash
pip install gradio seaborn scikit-learn pandas matplotlib pillow
```

2. **Run the script**:

Paste the entire code block into your Colab or Python environment and run it. It will launch a **Gradio web interface**.

3. **Upload a CSV file** containing your sensor data.

4. **View outputs**:
   - Model accuracy and metrics
   - Confusion Matrix
   - Feature importance bar chart

## 📌 Notes

- The model automatically detects the activity label column.
- All numerical columns are treated as features (accelerometer + gyroscope).
- The Random Forest model is re-trained on every file upload.

## 💡 Future Improvements
- Add support for time-series models (e.g., LSTM, CNN).
- Live sensor streaming and real-time classification.
- Export trained model for mobile/embedded deployment.
- Cross-validation and comparison with other classifiers.

## 📬 Author
Created as part of a project exploring machine learning applications in human activity recognition.
