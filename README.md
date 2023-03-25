# NECSTCAMP_NL1_BioImage
This project was assigned to me at the end of the biomedical computer vision course taught at the NECST lab of the Politecnico di Milano. The code reported on a colab file is written in python, and the goal of the project is to train a neural network (in this case, U-NET), through the use of several libraries, to distinguish from an abdominal MRI dataset the kidneys and, if present, any tumors.

# Dataset Consideration
The dataset is the following: https://github.com/neheller/kits19

I only work on the 100 first patients due to memory problems related to colab and drive in their free versions.
Most of the images in the dataset are 512x512 in size, in any case, since colab in its free version is not very performing, I preferred to rescale the images to 256x256, the minimum present among the top 100 patients.

#Binary Segmentation
The colab file is the one that contains the actual code, where I perform a type of binary segmentation, eliminating in the masks the distinction between kidneys and tumors, setting everything that is background to 0 and setting everything that is other than background to 1. Binary segmentation was not sufficient for the identification of tumors alone, but sufficient for the identification of kidneys within MRI images. 
