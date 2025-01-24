# Kokoro-TTS

**Note:** This is not the official repository.<br> The written code is not well-organized.<br>

Alternative ways to use Kokoro-TTS [kokoro-onnx](https://github.com/thewh1teagle/kokoro-onnx), [Kokoro-FastAPI](https://github.com/remsky/Kokoro-FastAPI), [kokoro](https://github.com/hexgrad/kokoro), [kokoro-web](https://huggingface.co/spaces/webml-community/kokoro-web), [Kokoro-Custom-Voice](https://huggingface.co/spaces/ysharma/Make_Custom_Voices_With_KokoroTTS)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NeuralFalconYT/Kokoro-82M-WebUI/blob/main/Kokoro_82M_Colab.ipynb) <br>
[![HuggingFace Space Demo](https://img.shields.io/badge/🤗-Space%20demo-yellow)](https://huggingface.co/spaces/NeuralFalcon/Kokoro-TTS)


---

### Installation Tutorial

My Python Version is 3.10.9.

#### 1. Clone the GitHub Repository:
```bash
git clone https://github.com/NeuralFalconYT/Kokoro-82M-WebUI.git
cd Kokoro-82M-WebUI
```

#### 2. Create a Python Virtual Environment:
```bash
python -m venv myenv
```
This command creates a new Python virtual environment named `myenv` for isolating dependencies.

#### 3. Activate the Virtual Environment:
- **For Windows:**
  ```bash
  myenv\Scripts\activate
  ```
- **For Linux:**
  ```bash
  source myenv/bin/activate
  ```
This activates the virtual environment, enabling you to install and run dependencies in an isolated environment.
Here’s the corrected version of point 4, with proper indentation for the subpoints:


#### 4. Install PyTorch:

- **For GPU (CUDA-enabled installation):**
  - Check CUDA Version (for GPU setup):
    ```bash
    nvcc --version
    ```
    Find your CUDA version example ```11.8```

  - Visit [PyTorch Get Started](https://pytorch.org/get-started/locally/) and install the version compatible with your CUDA setup.:<br>
    - For CUDA 11.8:
    ```
    pip install torch  --index-url https://download.pytorch.org/whl/cu118
    ```
    - For CUDA 12.1:
    ```
    pip install torch  --index-url https://download.pytorch.org/whl/cu121
    ```
    - For CUDA 12.4:
    ```
    pip install torch  --index-url https://download.pytorch.org/whl/cu124
    ```
- **For CPU (if not using GPU):**
  ```bash
  pip install torch
  ```
  This installs the CPU-only version of PyTorch.


#### 5. Install Required Dependencies:
```bash
pip install -r requirements.txt
```
This installs all the required Python libraries listed in the `requirements.txt` file.

#### 6. Download Model and Get Latest VoicePack:
```bash
python download_model.py
```

---

#### 7. Install eSpeak NG

- **For Windows:**
  1. Download the latest eSpeak NG release from the [eSpeak NG GitHub Releases](https://github.com/espeak-ng/espeak-ng/releases/tag/1.51).
  2. Locate and download the file named **`espeak-ng-X64.msi`**.
  3. Run the installer and follow the installation steps. Ensure that you install eSpeak NG in the default directory:
     ```
     C:\Program Files\eSpeak NG
     ```
     > **Note:** This default path is required for the application to locate eSpeak NG properly.

- **For Linux:**
  1. Open your terminal.
  2. Install eSpeak NG using the following command:
     ```bash
     sudo apt-get -qq -y install espeak-ng > /dev/null 2>&1
     ```
     > **Note:** This command suppresses unnecessary output for a cleaner installation process.

---
#### 8. Install ffmpeg [Only For Linux Users]
Skip this step if you are using Windows.
You only need FFmpeg if you plan to use it for subtitle dubbing feature. If you just want to use *Kokoro TTS*, you can *skip* this step too.
```
  apt-get update
  !apt-get install -y ffmpeg
```

#### 9. Run Gradio App

To run the Gradio app, follow these steps:

1. **Activate the Virtual Environment:**
   ```bash
   myenv\Scripts\activate
   ```

2. **Run the Application:**
   ```bash
   python app.py
   ```

   Alternatively, on Windows, double-click on `run_app.bat` to start the application.

---

![1](https://github.com/user-attachments/assets/9907ed46-f943-4819-8f9b-6ec8666115d2)
![2](https://github.com/user-attachments/assets/79eba62f-5829-414e-8ce0-5420ecd134b5)
![3](https://github.com/user-attachments/assets/61a18dc0-6b11-41c0-b693-6cfaf18a9084)
![4](https://github.com/user-attachments/assets/f633045c-ce92-491f-9a83-58b07a12c583)
![5](https://github.com/user-attachments/assets/6ffaab71-7bbd-47a0-8a48-0c7ee4be3c85)

### License
[Kokoro model](https://huggingface.co/hexgrad/Kokoro-82M), is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)<br>
The inference code adapted from StyleTTS2 is MIT licensed.
### Credits
**Model:**
[Kokoro HuggingFace](https://huggingface.co/hexgrad/Kokoro-82M)

**Podcast Generation Inspiration:**
[E2-F5-TTS](https://huggingface.co/spaces/mrfakename/E2-F5-TTS)

**Voice Mix Feature:**
[Make Custom Voices With KokoroTTS](https://huggingface.co/spaces/ysharma/Make_Custom_Voices_With_KokoroTTS)

**AI Assistance:** <br>
[ChatGPT](https://chatgpt.com/)<br>
[Google AI Studio](https://aistudio.google.com/)<br>
[Github Copilot](https://github.com/features/copilot)<br>

