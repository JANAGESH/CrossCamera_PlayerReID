**Cross-Camera Player Re-Identification (YOLO + DeepSORT)**

This project enables cross-camera player re-identification using a fine-tuned YOLOv11 object detection model along with DeepSORT for player tracking. The notebook processes two synchronized videos (broadcast.mp4 and tacticam.mp4) to maintain consistent player IDs across both camera feeds — ideal for sports analytics.

**Google Drive Setup**

The pretrained YOLO model (best.pt) is stored in Google Drive. Make sure to mount your Google Drive in Colab and place the file accordingly.

🔗 Download best.pt from this Drive link : https://drive.google.com/drive/folders/14miSAujyZvaucxGRMJnK3mDnXMy93moL?usp=sharing

After downloading, upload best.pt to your own Drive, then mount it in Colab and set the path:

from google.colab import drive
drive.mount('/content/drive')

# Example path
model_path = "/content/drive/MyDrive/best.pt"

**Files Included**

CrossCamera_Player_ReID.ipynb – Main Colab notebook for tracking and re-identification

best.pt – Fine-tuned YOLOv11 model weights

Input Videos – broadcast.mp4 and tacticam.mp4 (you can upload via Colab or Drive)

**Install Dependencies**

Run the following in a Colab cell:

!pip install -q ultralytics filterpy opencv-python-headless matplotlib pandas

**Set correct paths to:**

best.pt

broadcast.mp4

tacticam.mp4

Run all cells in order.

Final output video with consistent player IDs will be saved to disk.

**Output**

Annotated video showing consistent player identities across cameras.

Visualization handled using OpenCV and pandas.

Notes:

The YOLOv11 model is custom-trained; re-training may be needed for other sports or teams.

Synchronization between video feeds is crucial for accurate matching.
