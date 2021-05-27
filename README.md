# A PyTorch implementation of 3D U-Net for filopodia segmentation

This is an PyTorch implementation of the 3D U-Net descibed in the paper: [3-D Quantification of Filopodia in Motile Cancer Cells](https://pubmed.ncbi.nlm.nih.gov/30296215/) by Castilla et al. (2017). 

The dataloader is optimized to take variable sized 3d data. Usually this data consists of crops of 3d confocal data of 1024x1024 px with a variable amount of z-stacks around 20. The data will be divided into similiarly sized pathches with overlap between adjacent patches (default patch size and overlap are 134 and 44 pixels, respectively). The overlap between patches allowes to stitch the output images to regain the original size back.
