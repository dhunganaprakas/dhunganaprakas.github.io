# About me

My name is Prakash Dhungana and I am a second year Computer Engineering Ph.D. student in the Department of Electrical and Computer Engineering at the University of Kentucky. I am currently pursuing my Ph.D. under the supervision of Dr. Sayed Ahmad Salehi at [Computing with Unconventional Technologies (CUT)](https://salehi.engr.uky.edu/cut-lab) laboratory. My primary research objective is to pledge robust and reliable training and inference of ML models for embedded platforms in real-time scenarios. Ultimately, I aim to create innovative solutions that empower these models to excel despite constraints, improving their ability to adapt and perform well in dynamic environments. I am planning to take my oral qualifying examination during the Fall of 2024, most probably in early November. Prior to my PhD, I obtained my Master's degree in Automotive Computing and Communications at University of Osijek (Croatia) in 2021 and Bachelor's in Mechanical Engineering at Tribhuvan University (Nepal) in 2016.    

In 2016, after graduating as a Mechanical engineer, I joined IME Motors, where I worked as an automotive service advisor for Ashok Leyland commercial vehicles. Later in 2018, I joined Goldfish International, where I worked as service engineer for SML ISUZU commercial vehicles. During those periods, I overlooked diagnosis, overhauling, manage service operations at a branch and later nation-wide and handle warranty claims. After my involvement in automotive service and diagnosis, I pursued further studies towards Automotive Computing in 2019 at University of Osijek (Croatia). After graduating from University of Osijek, I worked as an Embedded Software Developer at Time Triggered Technologies Auto (TTTech Auto), Osijek from 2021 before joining University of Kentucky in 2023 for my PhD.  

# Research Interests

* Embedded Systems
* Real Time Operating Systems
* Machine Learning, TinyML
* Embedded drivers and software
* Automotive Software
* Advanced Driver Assistance Systems (ADAS)
* Autonomous Driving
* Computer Vision

# Projects

## RTKWS: Real-Time Keyword Spotting

An efficient real-time keyword spotting (RTKWS) architecture for edge devices is designed and implemented. The proposed architecture comprises data acquisition (DA), silence detection, feature extraction (FE), and binary classification units. To minimize the required memory footprint and computational complexity, the architecture uses 8-bit integer voice data and performs all computations only in integers. The FE unit converts input data into 2-dimensional feature maps using a short-time Fourier transform (STFT) to be subsequently used by the classification unit. This unit uses a neural network model comprising three convolutional layers and one fully connected layer. The model is quantized using a new approach based on the quantization method in the TensorFlow lite (TFlite) tool. The model can be trained to accurately classify the feature maps for any pair of desired keywords. We implemented the architecture in pure C code with no external dependencies to make it portable to a general edge device. We deployed the architecture on a low-cost edge device, TM4C123GXL from Texas Instruments and achieved real-time operation.

![RTKWS Deployment Setup](/assets/publications/rtkws_deployment.bmp)

### Publications

* P. Dhungana and S. A. Salehi, ``Exploring the Effect of Kernel Depth in Compact Keyword Spotting Models," 2024 International Congress on Human-Computer Interaction, Optimization and Robotic Applications (HORA), Istanbul, Turkiye, 2024, pp. 1-6, [doi: 10.1109/HORA61326.2024.10550542](https://ieeexplore.ieee.org/document/10550542).

* P. Dhungana and S. A. Salehi, ``RTKWS: Real-Time Keyword Spotting Based on Integer Arithmetic for Edge Deployment," 2024 25th International Symposium on Quality Electronic Design (ISQED), San Francisco, CA, USA, 2024, pp. 1-7, [doi: 10.1109/ISQED60706.2024.10528680](https://ieeexplore.ieee.org/document/10528680).

* S. A. Salehi and P. Dhungana, ``A Low-cost keyword spotting architecture based on wavelet packets feature extraction for edge device," 2024 25th International Symposium on Quality Electronic Design (ISQED), San Francisco, CA, USA, 2024, pp. 1-1, [doi: 10.1109/ISQED60706.2024.10528719](https://ieeexplore.ieee.org/document/10528719).

## PCIe Backbone Communication


## Three Layered Sagety Services (3LSS) Integration


## Brightness and Color Equalization

Implements brightness and color equalization (BCE) methods of images obtained from different cameras on a real advanced driver assistance system (ADAS) platform. In particular, four different methods for BCE that are a combination of a basic linear transformation (BLT) and gamma correction are implemented and tested. In addition to BCE, blending operations based on improved gradual fusion were also carried out to obtain a smooth transition of brightness and color components in the final panoramic image at the overlapping region between the input images. The resulting images were tested subjectively to determine the most preferred method for BCE out of four methods. The developed solution for BCE was implemented on the ADAS ALPHA development board.

![Input provided to BCE Algorithm](/assets/publications/bce_output.png)


![Outputs from BCE Algorithm](/assets/publications/bce_output.png)

### Publications

* P. Dhungana, M. Herceg, R. Grbić and V. Marinković, ``Implementation of brightness and color equalization methods to create a smooth panoramic image on a real ADAS platform," 2022 International Symposium ELMAR, Zadar, Croatia, 2022, pp. 185-190, [doi: 10.1109/ELMAR55880.2022.9899793](https://ieeexplore.ieee.org/document/9899793).




