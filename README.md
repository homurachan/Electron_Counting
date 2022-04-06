# Electron_Counting
Electron counting programs for Falcon III camera.

Hybrid_electron_counting.exe is the program that generates counted images with Hybrid counting method. It is a standalone program and has been tested in Ubuntu 14.04/ 16.04/18.04/20.04. 

Usage: Hybrid_electron_counting.exe -i yourstack.mrc -m 'value_m' -x 'value_x' -p 'value_p' -O output.mrc

'value_m' and 'value_x' are voltage-dependent, maybe camera dependent, too. The suggested values are '-m 45 -x 35', '-m 30 -x 30', '-m 30 -x 25' for our 120/200/300-kV datasets. 'value_p' describes how many counted frames are simple summed before final output. Every frame is calculated separately, however, it was meaningless to output every single frame if per-frame dose was very low. We collected our data with about 0.01 electron/frame/pixel, as a result, the suggest 'value_p' was 30-50 for general data or 1 for debug usage. There are also some debug options, use the command 'Hybrid_electron_counting.exe -h' to see all available options.

Please cite our article if our algorithm or these programs are useful: An electron counting algorithm improves imaging of proteins with low-acceleration-voltage cryo-electron microscope, D.J. Zhu, H.G. Shi, C.L. Wu and X.Z. Zhang, Communications Biology (2022). DOI: 10.1038/s42003-022-03284-1

# Examples of raw image stacks
Single frame of 120/300kV raw images are presented in this repository. Here are two stacks below.

300kV with beamstopper, 39 frames, total of ~0.6 electron/pixel: https://drive.google.com/file/d/1TUbeOKZ7Tx7fzq2Qfe5FUalItxrLSZ4H/view?usp=sharing

120kV with beamstopper, 39 frames, total of ~0.5 electron/pixel: https://drive.google.com/file/d/1_24qEJvVAFiN6JNh5zNT0zrpKlpY-TW6/view?usp=sharing

As for the raw images of our datasets, we may gradually upload them to EMPIAR-CHINA. Since each dataset occupies more than 10TB of storage space, it would take forever to upload. You can contact the corresponding author and send us hard disks to get a copy of dataset.

# License
Copyright 2019-2022 Xinzheng Zhang & Dongjie Zhu.

The programs in this project are available free of charge for non-profit academic research.

For other use, please contact the corresponding author.

# Competing interests
A patent application on electron counting algorithm of Hybrid is pending.
