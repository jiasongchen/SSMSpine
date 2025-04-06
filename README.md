# SSMSpine
**SSMSpine** dataset comprises a total of **12,500** synthetic yet realistic mid-sagittal lumbar spine MR images. Each MRI is annotated with the identification of five lumbar discs **(D1, D2, D3, D4, D5)** and six vertebral bones **(L1, L2, L3, L4, L5, S1)**.SSMSpine provides not just annotated segmentation masks but also includes landmark coordinates, offering valuable information for diverse medical image analysis tasks.

Image size is **512 × 512**, and the intensity of each image is normalized to fall within the range **[0,1]**. The dataset also include intensity corrected images, intensity equalized images, pixel labels, masks, landmark points coordinates for each subject in images. There are **236** shape landmark points for each vertebra bone, and **176** shape landmark points for each lumbar disc.

The SSMSpine dataset is synthesized using a combination of a statistical shape model (SSM) and biomechanics, which serves as a special way of de-identifying patient image data. For details of the generation process, please refer to our paper ***[Evaluation of Deep Neural Network Models for Instance Segmentation of Lumbar Spine MRI](https://www.biorxiv.org/content/10.1101/2024.04.02.587810v1)***.

Kindly be aware that the SSMSpine dataset is exclusively intended for research purposes.

## Download Dataset

You can use direct links to download  [SSMSpine Dataset](https://drive.google.com/drive/folders/17QXBCrfcQB6Gc4ITZBAURHoD60AMEQBB?usp=drive_link).



| Name  | Content | Patient Texture | Virtual Shape | Virtual Patients | Size | Link |
| :---: | :---: | :---: | :---: | :---: |:---: | :---: |
| `SSMSpine_Train.zip`  | Train| 80 | 125 |10,000| 20.23GB | [Download](https://drive.google.com/file/d/1WkiMCZC5gz_zKf5cXHVwUw5uJCcFIRrM/view?usp=sharing)|
| `SSMSpine_Test.zip`  | Test| 20 | 125 | 2,500 | 5.19GB | [Download](https://drive.google.com/file/d/17Xp3fEIKo9h1VNMkEXzG5SWIRB8uol02/view?usp=sharing)|
| `SSMSpine_Train_Sample.zip` | Train samples | 1 | 125 | 125| 205.6MB | [Download](https://drive.google.com/file/d/1D2_j9wm7_E-SBQ53E6sIDi-q3gQZlB39/view?usp=drive_link)|
| `SSMSpine_Test_Sample.zip`  | Test samples | 1 | 125 | 125| 261.7MB | [Download](https://drive.google.com/file/d/1K7WtxCH3tvAanIRXVlReerrigM1iu21k/view?usp=drive_link)|

## Data Description

The data is organized as a dictionary. The following provides the data details.

| Key | Shape | Description |
| :---: |:---:| :---: |
| img | (512, 512)| Raw Image |
| img_corrected |(512, 512)|Corrected Image |
| img_equalized |(512, 512)| Equalized Image |
| label | (1, 512, 512) | Label |
| mask | (11, 512, 512) | All masks |
| shape | (1696, 2) | All Shape Landmark Points |
| bone | (6, 236, 2) | Bone Shape Landmark Points |
| bone_mask |(6, 512, 512)| Bone Masks |
| disk |(5, 176 ,2)| Disc Shape Landmark Points |
| disk_mask |(5, 512, 512)| Disc Masks |


### Labels
The description of image labels is as follows:

| Label | Description |
| :---: | :---: |
| 0 | Background |
| 1 | L1 |
| 2 | L2 |
| 3 | L3 |
| 4 | L4 |
| 5 | L5 |
| 6 | S1 |
| 7 | L1/L2 (D1) |
| 8 | L2/L3 (D2) |
| 9 | L3/L4 (D3) |
| 10 | L4/L5 (D4) |
| 11 | L5/S1 (D5) |

<img src="fig/2.jpg" width = "30%">


## Usage
 Load data with [torch.load( )](https://pytorch.org/)

## Sample Visualization
<img src="fig/1.jpg">


## CONTACT

To access the complete SSMSpine dataset, which is password-protected, kindly send an email to the jiasong.chen@miami.edu for further assistance.


## CITATION

```latex
@article{chen2024evaluation,
  title={Evaluation of Deep Neural Network Models for Instance Segmentation of Lumbar Spine MRI},
  author={Chen, Jiasong and Qian, Linchen and Ma, Linhai and Urakov, Timur and Gu, Weiyong and Liang, Liang},
  journal={bioRxiv},
  pages={2024--04},
  year={2024},
  publisher={Cold Spring Harbor Laboratory}
}
```
