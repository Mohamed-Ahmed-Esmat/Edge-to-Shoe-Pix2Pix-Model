# Edge-to-Shoe-Pix2Pix-Model
This repository contains an implementation of the Pix2Pix GAN model applied to the task of generating shoes from edge images. The model is trained to learn the mapping from sketches to realistic images of shoes using the Pix2Pix architecture.
## Dataset

The notebook utilizes the [Edges2shoes Dataset](https://www.kaggle.com/datasets/balraj98/edges2shoes-dataset), which contains a collection of shoes with its equivilant edges. The dataset is automatically downloaded and extracted using the Kaggle API.

## Prerequisites

Before running the notebook, ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- Kaggle API (configured with your credentials)

### Python Libraries

- `kaggle`
- `torch`
- `numpy`
- `matplotlib`
- `cv2`

You can install the required libraries using:

```bash
pip install kaggle torch numpy matplotlib cv2 
```

## Running the Notebook
1. Clone the repository:
```bash
git clone https://github.com/Mohamed-Ahmed-Esmat/Edge-to-Shoe-Pix2Pix-Model.git
```
2. Open the notebook
```bash
jupyter notebook pix2pix-edge-shoes.ipynb
```
3. Ensure your Kaggle API credentials are properly set up. The dataset will be downloaded automatically when you run the first cell of the notebook.
4. Execute the notebook cells to preprocess the dataset, define the Pix2Pix model, and begin training.
## Data Augmentation
In addition to the basic preprocessing, data augmentation was applied using a Conditional GAN (CGAN) in a separate notebook to generate additional shoe images. This augmented dataset is used to enhance the training of the Pix2Pix model. The augmentation process includes generating variations of shoe images from edge inputs, thus increasing the diversity of the training data.
The CGAN-based data augmentation steps are outlined in a different notebook included in the repository.
## Notebook Contents
The notebook is organized as follows:

1. **Dataset Download:** The dataset is downloaded from Kaggle using the Kaggle API and unzipped for further processing.
2. **Data Preprocessing:** The images are resized, normalized, and split into training and validation sets. Data augmentation with CGAN-generated shoe images is applied in a separate preprocessing step.
3. **Model Architecture:** The Pix2Pix is built using PyTorch, where the generator and discriminator networks are defined.
4. **Training:** The model is trained to generate shoes given edged images. Training is on 30 epochs.
5. **Evaluation and Results:** Generated images are visualized.

## Example Output:
Below are examples of the shoes given these edges:

<div>
  <h4>Input Edges:</h4>
  <img src="https://github.com/user-attachments/assets/566e01cb-b0df-4cb3-9a07-426f3c66226a" alt="Input Edges Shoes" width="400" />
</div>

<div>
  <h4>Output Shoes:</h4>
  <img src="https://github.com/user-attachments/assets/5ac70b02-d807-411a-86ff-bf57fe7336f4" alt="Generated Shoes" width="400" />
</div>


## Acknowledgements
- The project is based on [Image-to-Image Translation with Conditional Adversarial Networks](https://arxiv.org/pdf/1611.07004), introduced by Isola et al. (2017), which uses a Conditional GAN for image-to-image translation tasks.
## Licenses
This project is licensed under the MIT [`LICENSE`](LICENSE) - see the LICENSE file for details.
