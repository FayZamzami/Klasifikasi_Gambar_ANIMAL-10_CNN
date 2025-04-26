# 🦁 Animal Image Classifier (Animals-10)

## 📖 Ringkasan
Implementasi end-to-end pipeline klasifikasi 10 jenis hewan dari dataset **Animals-10** menggunakan **MobileNetV2** sebagai feature extractor. Mulai dari eksplorasi data, preprocessing & augmentasi, pelatihan model, evaluasi, hingga konversi ke **SavedModel**, **TensorFlow Lite**, dan **TensorFlow.js**, plus fitur prediksi interaktif.

---

## 👥 Penulis
- **Nama:** Fayadh Rizqi Zamzami  
- **Email:** _farizam1504@gmail.com_  
- **Institusi:** Universitas Brawijaya  

---

## 🛠️ Teknologi & Library
- **Deep Learning:** TensorFlow 2.x, Keras  
- **Data Handling:** pandas, numpy  
- **Visualisasi:** matplotlib, seaborn  
- **Image I/O:** Pillow, OpenCV  
- **Utility:** scikit-learn, tqdm  
- **Deployment:** tensorflowjs, tkinter (GUI prediksi)  

---

## 🚀 Alur Kerja

1. **Pengumpulan & Eksplorasi Data**  
   - Hitung total gambar per kelas  
   - Visualisasi distribusi label  
   - Random sample grid & Error Level Analysis (ELA)

2. **Preprocessing & Augmentasi**  
   - Split 80% train / 10% validation / 10% test  
   - Normalisasi (0–1) & augmentasi (rotasi, zoom, shift, flip)

3. **Membangun & Melatih Model**  
   - **MobileNetV2** (pretrained) + lapisan CNN tambahan  
   - Adam optimizer, categorical crossentropy  
   - Callback: EarlyStopping, ModelCheckpoint, ReduceLROnPlateau  

4. **Evaluasi**  
   - Plot akurasi & loss (train vs validasi)  
   - Classification report & confusion matrix  
   - Visualisasi prediksi acak di test set  

---

## 📊 Hasil Akhir
- **Test Accuracy:** 94.88%  
- **Model Sizes:**  
  - SavedModel: `saved_model/`  
  - TFLite: `tflite/model.tflite` (~ KB/MB)  
  - TFJS: `tfjs_model/model.json` + shard binaries  

---
