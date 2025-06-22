
# 🧠 Image Classification Using SVM

This project demonstrates how to build an image classification system using **Support Vector Machines (SVM)** with **scikit-learn**. It classifies images into one of three categories:

- Ferrari 250 GTO
- Cricket Bat
- Dragon Fruit

Images are downloaded automatically using the **Bing Image Downloader**.

---

## 🚀 Features

- 🔽 Automatic image dataset creation using `bing-image-downloader`
- 🖼️ Preprocessing using `scikit-image`
- 🤖 SVM model with GridSearchCV tuning
- 💾 Model saved and loaded using `pickle`
- 📸 Predict image category from a URL input
- 📊 Evaluation metrics like accuracy and confusion matrix

---

## 📁 Dataset

Images are downloaded and saved into:

```
images/
├── Ferrari 250 GTO/
├── Cricket Bat/
└── Dragon Fruit/
```

Each class has ~25 images (can be adjusted).

---

## 🛠️ Requirements

Install all dependencies via pip:

```bash
pip install bing-image-downloader scikit-image matplotlib scikit-learn numpy pillow requests
```

---

## 🧪 Training the Model

Run the script to:

1. Download images
2. Preprocess them
3. Train an SVM classifier
4. Save the model as `img_model.p`

```python
from bing_image_downloader import downloader
downloader.download('Ferrari 250 GTO', limit=25, output_dir='images', adult_filter_off=True)
...
```

---

## 📈 Model Evaluation

You can print:

- Accuracy score
- Confusion matrix
- Classification report

Example:
```python
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
```

---

## 🔍 Make Predictions from URL

The model can classify a new image from a direct URL:

```python
url = input("Enter image URL: ")
img = imread(url)
# preprocess...
y_out = model.predict(test_data)
```

Prediction will be printed and the image displayed using `matplotlib`.

---

## 📂 Output

Example Output:

```
Predicted Output: Ferrari 250 GTO
```

![Example Image](https://your_image_url_here.jpg)

---

## 💡 Future Improvements

- Replace SVM with deep learning (e.g. MobileNet, ResNet)
- Use Gradio or Streamlit for UI
- Add webcam image capture
- Include more categories with balanced samples

---

## 🔒 License

This project is under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Avinash Telikicherla**  
Feel free to connect for suggestions or improvements.
