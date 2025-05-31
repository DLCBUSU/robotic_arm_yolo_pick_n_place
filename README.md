Robotic Arm Pick and Place dengan Deteksi Visual Machine Learning (YOLOv11)
Sistem edukatif integratif yang memadukan robotika, deteksi objek berbasis YOLOv11, dan GUI Python interaktif dalam satu proyek.

📌 Deskripsi
Repositori ini berisi dokumentasi dan kode sumber dari proyek pembelajaran bertema Robotic Arm Pick and Place Berbasis Deteksi Visual. Sistem ini mengenali objek berbentuk bola dalam tiga warna (merah, kuning, hijau) menggunakan model YOLOv11, kemudian menggerakkan lengan robotik 3 DOF untuk mengambil dan memindahkan objek secara otomatis berdasarkan hasil klasifikasi warna.

Sistem ini dirancang untuk tujuan edukasi dalam bidang AIoT, robotika, dan machine learning.

🧠 Stack Teknologi

Gambar 1. Stack Teknologi Sistem Robotic Arm Pick and Place Berbasis Machine Learning

Hardware:

Robotic Arm 3 DOF (dengan motor stepper + driver A4988)

Arduino Mega (kontrol aktuator dan pompa)

End-effector vacuum pump

Kamera USB

Software:

YOLOv11 (PyTorch)

Python (OpenCV, Serial, GUI)

Arduino IDE

🖼️ Dokumentasi Visual
Tampak Depan Robot	Tampak Samping + End-effector

Gambar 2. Tampak Depan Robot Arm 3-DOF yang Telah Dirakit	

Gambar 3. Tampak Samping Robot Arm 3-DOF dengan End-Effector

GUI Deteksi Visual

Gambar 4. Tampilan GUI saat mendeteksi objek bola warna merah

📁 Struktur Direktori
bash
Copy
Edit
├── arm_robot_mega/                  # Program Arduino (Arduino Mega)
│   └── robotic_arm_controller.ino
├── python/
│   ├── arm_robot.py                 # Kontrol logika robotik berbasis deteksi
│   ├── gui.py                       # GUI utama + koneksi ke Arduino + YOLO inference
│   └── dataset_capture.py          # Ambil dataset dari kamera USB
├── model/
│   └── yolo_bola.pt                # Model YOLOv11 untuk deteksi bola warna
├── gambar/
│   ├── stack_teknologi.png
│   ├── robot_depan.png
│   ├── robot_samping.png
│   └── gui_deteksi_merah.png
└── README.md
🚀 Cara Menjalankan
1. Siapkan Perangkat Keras
Rakit lengan robotik sesuai wiring diagram

Hubungkan Arduino Mega ke PC

Hubungkan kamera USB

2. Upload Program Arduino
bash
Copy
Edit
# Gunakan Arduino IDE
Buka dan unggah: arm_robot_mega/robotic_arm_controller.ino
3. Install Dependensi Python
bash
Copy
Edit
pip install -r requirements.txt
Atau manual:

bash
Copy
Edit
pip install torch torchvision opencv-python pyserial pillow
4. Jalankan GUI Utama
bash
Copy
Edit
cd python
python gui.py
(Opsional) Tangkap Dataset Baru
bash
Copy
Edit
python dataset_capture.py
🧪 Fitur Unggulan
Deteksi objek bola berwarna secara real-time dengan YOLOv11

GUI interaktif untuk menampilkan hasil deteksi dan status robot

Eksekusi otomatis pick and place berdasarkan hasil deteksi

Dokumentasi lengkap dan folder terstruktur untuk pengembangan lanjutan

📖 Referensi
YOLOv11: https://github.com/WongKinYiu/yolov11

Roboflow: https://roboflow.com

✍️ Kontribusi
Proyek ini merupakan bagian dari konten pembelajaran robotika berbasis AI. Silakan fork dan kembangkan untuk keperluan pendidikan, riset, atau pengembangan mandiri.

📄 Lisensi
Lisensi MIT – Bebas digunakan untuk tujuan edukatif dan non-komersial.
