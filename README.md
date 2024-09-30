# 3D Image Resolution Enhancement

User-friendly framework for imaging resolution enhancement. This framework has been built to help prepare imaging data to facilitate the use of the deep-learning-based tool CARE (3D)[2], which supports supervised image restoration and resolution enhancement in 3D images. This tool is based on the ZeroCostDL4Mic CARE repository [1]. Additionally, to build the current framework, we based it on the ZeroCost repository structure and consists of a collection of self-explanatory Jupyter Notebooks for Google Colab.


## Google Colab Files
**3D_image_resolution_enhancement** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1gp6wwgfXoAKGWdehBVKbYdGabOzMS009?authuser=1) or [set_dimensions.ipynb](Colab_notebooks/set_dimensions.ipynb)\
This notebook facilitates the conversion of original images stored in '.lif' (Leica Image File Format) or '.czi' (Carl Zeiss Image) formats to the widely compatible '.tiff' (Tagged Image File Format).

Step 1. The first step you have to set up the paths in section
Set up the paths
Step 2. Go to correscopding section to convert raw image:
2-A. to convert lif to tif
2-B. to convert czi to tif
2-C. to convert tilescan czi to tif
There are optional sections that to reconstruct the 4D(multi-channle) or 5D(time-lapse movie) image: -
base_path: this is the path where your original image is located in your google drive, and where the output will be saved.

input_file: this is the name of your original image file.

output_folder: this is the folder to save the output files

make_folder: if set true, it will automatically create the output folder when it is not found in the base_path.

Further instructions can be found in the notebook.

## REFERENCES
### 1. ZeroCostDL4Mic
von Chamier, L., Laine, R. F., Jukkala, J., Spahn, C., Krentzel, D., Nehme, E., Lerche, M., Hernández-Pérez, S., Mattila, P. K., Karinou, E., Holden, S., Solak, A. C., Krull, A., Buchholz, T. O., Jones, M. L., Royer, L. A., Leterrier, C., Shechtman, Y., Jug, F., Heilemann, M., … Henriques, R. (2021). **Democratising deep learning for microscopy with ZeroCostDL4Mic. Nature communications, 12(1), 2276.**
[https://doi.org/10.1038/s41467-021-22518-0](https://www.nature.com/articles/s41467-021-22518-0)
### 2. CARE(3D)
Weigert, M., Schmidt, U., Boothe, T., Müller, A., Dibrov, A., Jain, A., Wilhelm, B., Schmidt, D., Broaddus, C., Culley, S., Rocha-Martins, M., Segovia-Miranda, F., Norden, C., Henriques, R., Zerial, M., Solimena, M., Rink, J., Tomancak, P., Royer, L., Jug, F., … Myers, E. W. (2018). **Content-aware image restoration: pushing the limits of fluorescence microscopy. Nature methods, 15(12), 1090–1097.** 
[https://doi.org/10.1038/s41592-018-0216-7](https://www.nature.com/articles/s41592-018-0216-7)
