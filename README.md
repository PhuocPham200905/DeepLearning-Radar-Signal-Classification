Markdown
## ⚙️ Installation & Configuration

### Prerequisites
Before you begin, ensure you have the following installed:
- **Python** 3.8 or higher
- **Anaconda** or **Miniconda** (highly recommended for environment management)
- **Git**

### Environment Setup
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/PhuocPham200905/DeepLearning-Radar-Signal-Classification.git](https://github.com/PhuocPham200905/DeepLearning-Radar-Signal-Classification.git)
   cd DeepLearning-Radar-Signal-Classification
Create and activate a virtual environment:

Bash
conda create -n radar-dl python=3.10 -y
conda activate radar-dl
Install dependencies:
(Assuming you have a requirements.txt file. If not, you will need to install libraries like torch, torchvision, numpy, matplotlib, etc., manually).

Bash
pip install -r requirements.txt


📊 Dataset Setup
This project utilizes the Radar & Communication Signal Data 2026 dataset.

Dataset Link: Kaggle - radarcommunsignaldata2026train

Option 1: Manual Download
Visit the Kaggle link above.

Click the Download button.

Extract the downloaded .zip file.

Move the extracted data into a data/raw/ directory within this project.

Option 2: Download via Kaggle CLI (Recommended)
If you prefer using the command line, you can download the dataset directly using the Kaggle API.

Install the Kaggle library:

Bash
pip install kaggle
Authenticate: Ensure your kaggle.json API key is placed in the correct directory:

Linux/Mac: ~/.kaggle/kaggle.json

Windows: C:\Users\<Your-Username>\.kaggle\kaggle.json

(Make sure to change the permissions of the file on Linux/Mac: chmod 600 ~/.kaggle/kaggle.json)

Download and extract the dataset:
Run the following commands from the root of your project directory:

Bash
# Create a directory for the dataset
mkdir -p data/raw
cd data/raw

# Download the dataset
kaggle datasets download -d huynhthethien/radarcommunsignaldata2026train

# Unzip the downloaded file (Linux/Mac)
unzip radarcommunsignaldata2026train.zip

# Return to the root directory
cd ../..
Expected Directory Structure
After downloading and extracting, your project structure should look similar to this before you start the training pipeline:

Plaintext
DeepLearning-Radar-Signal-Classification/
├── data/
│   └── raw/
│       ├── (extracted dataset folders/files go here)
├── models/
├── notebooks/
├── train.py
├── README.md
└── requirements.txt
🚀 Running the Project
Once the environment is configured and the dataset is placed in the data/raw folder, you can configure your training scripts (e.g., updating paths in your config file) and begin training the CNN model.
