# 3D Image Resolution Enhancement

User-friendly framework for imaging resolution enhancement. This framework has been built to help prepare imaging data to facilitate the use of the deep-learning-based tool CARE (3D)[2], which supports supervised image restoration and resolution enhancement in 3D images. This tool is integrated into the ZeroCostDL4Mic repository [1]. Additionally, to build the current framework, we based it on the ZeroCost repository structure and consists of a collection of self-explanatory Jupyter Notebooks for Google Colab.

The initial step in this pipeline involves file format conversions to ensure compatibility with the CARE tool, which exclusively processes ‘.tiff’ images. This transformation enables the conversion of widely used ‘.czi’ and ‘.lif’ image formats, commonly encountered in microscopy-based research. To achieve this, a folder in Google Drive must be created, and the images to be converted should be copied into that folder. Then, the **'Image Format Conversion to '.tiff' Format' notebook (located in the 'Google Colab Files' section)** has to be executed by following the provided instructions.

For training the CARE(3D) model, image pairs are imperative, comprising a low-resolution counterpart and an equivalent high-resolution image, both sharing identical dimensions. In the scenario where only high-resolution images are available, the virtual generation of lower-resolution image pairs can be obtained by employing the **'Virtual Low-Resolution Dataset Generation' notebook (located in the 'Google Colab Files' section)**, following the provided instructions.

If low-resolution image pairs are available but need to match the high-resolution image dimensions for training a CARE(3D) model, or if a trained model is accessible for prediction but input images for prediction do not correspond in dimension to the training images, the **'Image Dimensions Adjustments' notebook (located in the 'Google Colab Files' section)** can be executed following the provided instructions.

Addressing limited datasets, where the number of images is insufficient for model training, an augmentation process can be executed using the **'Dataset Augmentation' notebook (located in the 'Google Colab Files' section)**, following the provided instructions.

Finally, to train a model or make predictions with CARE(3D) using the output images obtained with this pipeline, the **'Adapted CARE(3D) Tool for Image Resolution Enhancement' notebook (located in the 'Google Colab Files' section)** can be executed following the provided instructions. The pipeline is designed to obtain two datasets named 'train_up' and 'train_down,' corresponding to the high-resolution images and low-resolution images, respectively. These paired datasets are necessary to train a CARE(3D) model. Depending on the options chosen by the user to execute this pipeline, the final datasets may have different names or structures. The key requirement is to have 'train_up' and 'train_down' folders containing pairs of images to train a model. Additionally, 'test_up' and 'test_down' folders can be obtained by extracting images from the 'train_up' and 'train_down' folders (the same images cannot be used for both training and testing). The folder structure required for inputting data into the CARE tool is also explained in the notebook.


## Google Colab Files
**Image Format Conversion to '.tiff' format:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ChzgxBgg9f5qBRLxkSh5es-lsRLe8F9L?usp=sharing)

**Image Dimensions Adjustments:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1tjP1P5_z5y1E9DP2LiHUXAzedx2V4fsl?usp=sharing)

**Virtual Low-Resolution Dataset Generation:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1tDA1cFFU_3kJSLmap_Z-nLUNbKaEV-xm?usp=sharing)

**Dataset Augmentation:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Nr0LxshkMI4wu5SImXkL9Rn6a7BLWl95?usp=sharing)

**Adapted CARE(3D) Tool for Image Resolution Enhancement:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1MApAuornmXibImudb2FggDYm3hYmagd5?usp=sharing)

#### ***Making changes to the notebooks**:
<font size = 3>You can make a copy of each notebook and save it to your Google Drive. To do this click file -> save a copy in drive.

#### ***GPU access**:
<font size = 3> To use the "Adapted CARE(3D) Tool for Image Resolution Enhancement" notebook to train a model or to predict new data, you will need to have GPU access (check Google colab resorces)


## REFERENCES
### 1. ZeroCostDL4Mic
von Chamier, L., Laine, R. F., Jukkala, J., Spahn, C., Krentzel, D., Nehme, E., Lerche, M., Hernández-Pérez, S., Mattila, P. K., Karinou, E., Holden, S., Solak, A. C., Krull, A., Buchholz, T. O., Jones, M. L., Royer, L. A., Leterrier, C., Shechtman, Y., Jug, F., Heilemann, M., … Henriques, R. (2021). **Democratising deep learning for microscopy with ZeroCostDL4Mic. Nature communications, 12(1), 2276.**
[https://doi.org/10.1038/s41467-021-22518-0](https://www.nature.com/articles/s41467-021-22518-0)
### 2. CARE(3D)
Weigert, M., Schmidt, U., Boothe, T., Müller, A., Dibrov, A., Jain, A., Wilhelm, B., Schmidt, D., Broaddus, C., Culley, S., Rocha-Martins, M., Segovia-Miranda, F., Norden, C., Henriques, R., Zerial, M., Solimena, M., Rink, J., Tomancak, P., Royer, L., Jug, F., … Myers, E. W. (2018). **Content-aware image restoration: pushing the limits of fluorescence microscopy. Nature methods, 15(12), 1090–1097.** 
[https://doi.org/10.1038/s41592-018-0216-7](https://www.nature.com/articles/s41592-018-0216-7)