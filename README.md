# Player-Re-Identification-in-a-Single-Feed



```markdown
# 🏃‍♂️ Player Re-Identification in a Single Feed

## 🎯 Objective

This project performs real-time **player tracking and re-identification** in a single 15-second video using a fine-tuned [YOLOv8](w) model and the [Deep SORT](w) tracking algorithm. It ensures players retain the same identity (ID) even after leaving and re-entering the frame.

---

## 📂 Project Structure

```

 ---
 ```
player\_reid\_single\_feed/

├── player\_tracking.ipynb          # Main Colab Notebook

├── best.pt                        # Trained YOLOv8 detection model

├── input\_15sec_input_720p.mp4                 # Input video file (15 seconds)

├── output\_tracked.mp4            # Output video with tracking boxes and IDs

├── report.pdf                     # Project methodology and insights

└── README.md                      # This file

````

---

## ⚙️ Setup & Execution

### ✅ Environment Requirements

- Python 3.8+
- Google Colab or Local Python environment
- Recommended: GPU (for faster inference)

### 📦 Dependencies

The following Python libraries are required:

```bash
pip install ultralytics opencv-python-headless filterpy deep_sort_realtime
````

> ⚠️ `opencv-python-headless` is used for compatibility with Colab environments. You may use `opencv-python` if running locally.

---

### ▶️ How to Run in Google Colab

1. **Upload Required Files**:

   * `best.pt` (YOLOv8 fine-tuned model)
   * `15sec_input_720p.mp4` (input soccer video)

2. **Open and Run the Notebook**:
   Use `player_tracking.ipynb`, which includes:

   * Model loading
   * Player detection using YOLOv8
   * Player ID tracking with Deep SORT
   * Export of the final video (`output_tracked.mp4`)

3. **Output**:

   * The resulting video with consistent Player IDs will be saved in Colab's `/content/output_tracked.mp4`

---

## 📌 Features

* Detects and tracks players frame-by-frame
* Maintains same ID for players who re-enter after leaving the frame
* Debug overlays: detection count and frame number
* Modular code structure for easy reuse and tuning

---

## 🔍 Notes

* Class `0` is assumed to be "player" in the YOLO model
* You can adjust confidence threshold or tracking parameters as needed
* If players are still missed, consider retraining the model or tuning `DeepSort` parameters

---

## 👤 Authors

* Bandi Poorna Sri Sailaja
* Project by: [Liat AI](https://liatai.com)

---

## 📄 License

This project is submitted as part of an AI internship task and is intended for evaluation purposes only.

```


