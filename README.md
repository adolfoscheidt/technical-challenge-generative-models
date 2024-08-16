# Meander Channel VAE

This project implements Variational Autoencoders (VAEs) to generate new images of meander-type geological channels. The dataset consists of 50,000 images of size 128x128 pixels, where yellow (1) represents the channel class and blue (0) represents the non-channel class. Two types of VAEs are explored: Convolutional + Dense and Fully Convolutional. This project is developed as a technical challenge proposed by LTrace company.

## Project structure
```bash
├── data                      # Directory to store the dataset
├── meander-channel-vae.ipynb # Jupyter Notebook with the implementation of the VAEs
├── models                    # Directory to save the model weights
└── requirements.txt          # Python dependencies
```

## Requirements

To avoid dependency conflicts, it's recommended to use a Python virtual environment.

### Setting up a Virtual Environment

1. Create a virtual environment:
   ```bash
   python3 -m venv venv
   ```
2. Activate the virtual environment:
    - on macOS/Linux:
    ```bash
    source venv/bin/activate
    ```
    - on Windows:
    ```bash
    venv\Scripts\activate
    ```
3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
## Usage
1. Data Preparation:

    The dataset `train_images.h5` is too large to be together with this repo; you have to download it and place the file inside the `data` directory. The dataset can be downloaded from this link: [train_images.h5](https://grrjnyzvhu1t.objectstorage.sa-saopaulo-1.oci.customer-oci.com/p/jfIQ-fCMHmA5jLi-DdqEIenJTzARdTp61YIzlDpRBi531v05mmWObjM2F1CBTIVL/n/grrjnyzvhu1t/b/General_ltrace_files/o/deep_esmda/train_images.h5)

2. Training the VAE Models:

- Open the `meander-channel-vae.ipynb` notebook.
- Run through the cells to train the Convolutional + Dense VAE and Fully Convolutional VAE.
- Model weights will be saved in the `models` directory.

3. Generating New Images:

- After training, the models can be used to generate new images of meander-type geological channels from the latent space.

## References

- [Variational Autoencoder Example - Keras](https://keras.io/examples/generative/vae/)
- [Understanding Variational Autoencoders (VAEs)](https://towardsdatascience.com/understanding-variational-autoencoders-vaes-f70510919f73)
- [Convolutional Neural Network (CNN) Explained](https://poloclub.github.io/cnn-explainer/)


