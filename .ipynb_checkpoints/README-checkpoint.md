# ⚙️ Want to Run on your machine? You need extra Data Setup!

## ⚠️ Prerequisite: Download the Dataset

For the analysis scripts to run, you must first download the required data and place it in the project's root folder. The **`data/`** folder is ignored by Git, so you must perform this step manually or use the provided automation script.

#### Manual Download Instructions

1.  **Visit the Kaggle Dataset Page:**
    Navigate to the following URL:
    [**AIM Dataset for Minecraft**](https://www.kaggle.com/datasets/finalboolean/aim-dataset-for-minecraft)

2.  **Download the Data:**
    Download two data files on the Kaggle page: `cheater.csv` and `legit.csv`.

3.  **Extract and Place Files:**
    * **Create a new directory** named **`data/`** in the root of this project.
    * **Extract** the downloaded ZIP file and place the necessary files (`cheater.csv` and `legit.csv`) directly inside the **`data/`** folder.

The final project structure should look like this:

```bash
unsupervised-minecraft-aimbot/
├── data/
│ ├── cheater.csv
│ └── legit.csv
├── README.md
└── EDA.ipynb
└── (and more...)
```

## ✨ Automated Download (when you've already set up your Kaggle client)

To simplify the data setup, we recommend using the automated Python script: **`automated_download.py`**.

* **Recommendation:** Use a standard Python file (`.py`) for the automation script, as it's easier to execute directly than a Jupyter Notebook.

#### How to Use the Automation Script

1.  **Install the Kaggle API Client:**
    ```bash
    pip install kaggle
    ```
2.  **Set up Kaggle API Token (Required):**
    * You must have a **Kaggle account** and generate an **API token** (`kaggle.json`) from your account settings.
    * Place the `kaggle.json` file in the correct location (e.g., `~/.kaggle/` on Linux/macOS or `%USERPROFILE%\.kaggle\` on Windows).
3.  **Run the Script:**
    Execute the Python script from the project root:
    ```bash
    python automated_download.py
    ```

The script will automatically download the dataset, authenticate using your token, extract the required files into the **`data/`** folder, and clean up the temporary ZIP file.