# 🧥 Fashion MNIST Classifier

A Convolutional Neural Network (CNN) built using TensorFlow/Keras to classify images from the Fashion MNIST dataset — including T-shirts, trousers, sneakers, and more.

---

## 📦 <u>Dataset:</u>
- Fashion MNIST (from tf.keras.datasets)
- 60,000 training images, 10,000 test images
- 10 classes:
````
0 - T-shirt/top       5 - Sandal  
1 - Trouser           6 - Shirt  
2 - Pullover          7 - Sneaker  
3 - Dress             8 - Bag  
4 - Coat              9 - Ankle boot
````

---

## 🧠 <u>Model Architecture:</u>
````
Sequential([
    Conv2D(32, (3,3), activation='relu', input_shape=(28, 28, 1)),
    MaxPooling2D(2, 2),
    Conv2D(64, (3,3), activation='relu'),
    MaxPooling2D(2,2),
    Flatten(),
    Dense(128, activation='relu'),
    Dense(10, activation='softmax')
])
````

---

## ⚙️ <u>Training Details:</u>
- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Epochs: 5
- Batch Size: 64 → 256 (experimentation)
- Preprocessing: Normalization (pixel / 255), Prefetching with AUTOTUNE

---

## 🧪 <u>Results:</u>

| Metric        | Value | 
|---------------|------|
|Final Test Accuracy|0.9017|
|Final Test Loss|0.2702|
|✅Loaded Model Accuracy|0.9017|

---

## 📈 <u>Sample Predictions:</u>

Predicted vs True (first 5 test images):
✅ All predictions matched the ground truth labels.

---

## 💾 <u>Model Saving & Loading</u>
- Saved using model.save("fashion_model.h5")
- Loaded using load_model("fashion_model.h5")
- Accuracy retained after loading: ✅

---

## 📌 <u>Highlights:</u>
- Used TensorFlow’s tf.data pipeline for efficient loading 
- Verified GPU availability (though training done on CPU for macOS)
- Discussed training speedups: large batch sizes, prefetching
- Ready for further experiments like regularization or dropout

---