# 🦁 Animal Image Classifier (Animals-10)

## 📖 Ringkasan
Implementasi end-to-end pipeline klasifikasi 10 jenis hewan dari dataset **Animals-10** menggunakan **MobileNetV2** sebagai feature extractor. Mulai dari eksplorasi data, preprocessing & augmentasi, pelatihan model, evaluasi, hingga konversi ke **SavedModel**, **TensorFlow Lite**, dan **TensorFlow.js**, plus fitur prediksi interaktif.

---

## 👥 Penulis
- **Nama:** Fayadh Rizqi Zamzami  
- **Email:** _your.email@example.com_  
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

## 📂 Struktur Direktori
. ├── animal_dataset/raw-img/ # folder gambar per kelas ├── saved_model/ # hasil export TensorFlow SavedModel ├── tflite/ # model .tflite + label.txt ├── tfjs_model/ # model web (TFJS) └── notebook.ipynb # Jupyter notebook utama


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

5. **Konversi untuk Deployment**  
   - **SavedModel** (server/cloud)  
   - **TensorFlow Lite** (mobile/embedded) + `label.txt`  
   - **TensorFlow.js** (browser)  

6. **Prediksi Interaktif**  
   - GUI sederhana (Tkinter) untuk memilih gambar  
   - Tampilkan gambar & hasil klasifikasi  

---

## 📊 Hasil Akhir
- **Test Accuracy:** _isi di sini (misal 92.5%)_  
- **Model Sizes:**  
  - SavedModel: `saved_model/`  
  - TFLite: `tflite/model.tflite` (~ KB/MB)  
  - TFJS: `tfjs_model/model.json` + shard binaries  

---
