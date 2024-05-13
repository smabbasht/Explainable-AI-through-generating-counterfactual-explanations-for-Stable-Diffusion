# EE 452: Project
## Explainable AI through generating counterfactual explanations for Stable Diffusion
This is a companion  repository titled after our associated research paper

## Initial Setup

In this section, we will prepare the necessary files and configurations required to run the project. We will download and upload various components such as the ResNetV2 classifier, the CelebA-HQ dataset, and the diffusion model checkpoints. Follow these steps to set up your environment properly.

### Step 1: Downloading and Uploading Files

1. **ResNetV2 Classifier:**
   - Download the ResNetV2 classifier model file. This file should be a trained model checkpoint that is compatible with PyTorch.
   - Upload the file to your Google Colab session. 
   - Move the uploaded file to the `/content/classifier` directory using the following command:
     ```bash
     !mkdir -p /content/classifier
     !mv path_to_your_uploaded_classifier_file /content/classifier/
     ```

2. **CelebA-HQ Dataset:**
   - Download the CelebA-HQ dataset. This dataset can typically be found on websites like Kaggle or directly from the original source that hosts this dataset.
   - Due to the large size of the dataset, it's recommended to upload it to your Google Drive.
   - Mount your Google Drive in this notebook:
     ```python
     from google.colab import drive
     drive.mount('/content/drive')
     ```
   - Ensure that the dataset is accessible at `/content/drive/MyDrive/path_to_celebA-HQ/`. You can create a symbolic link to make it accessible under `/content/data`:
     ```bash
     !ln -s /content/drive/MyDrive/path_to_celebA-HQ /content/data
     ```

3. **Diffusion Model Checkpoints:**
   - Download the checkpoints for your diffusion model. These are typically provided by the model developers or through a community repository.
   - Upload these checkpoints to your Colab session.
   - Move them into the `/content/diffusion` directory:
     ```bash
     !mkdir -p /content/diffusion
     !mv path_to_your_uploaded_diffusion_model_checkpoint /content/diffusion/
     ```

### Step 2: Verifying File Locations

After uploading and moving the files, it's a good practice to verify that everything is in the correct location. Use the following command to check the contents of each directory:

```bash
!ls /content/classifier
!ls /content/data
!ls /content/diffusion

