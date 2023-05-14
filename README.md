# Optimization-of-Image-inpainting-GANs
Optimization of image in-painting techniques by reduced precision training.

# Deep-Learning-Mini-Project


## Goal

##### Optimize image inpainting techniques: PD-GANs and Progressive-Generative-Networks by analysing models and identifying bottlenecks across different GPUs (Nvidia V100, Nvidia A100).

## Our Proposed Solution

### Using mixed precision training to improve per iteration training time while also improving overall energy efficiency 

![Alt text](arch.png)

## Repository Structure - below are the major contributions along with granular changes in various files of PD-GAN.

- `PD_GAN/` 
  - `optimization/` - All optimizations -  contributed by our team.
   - `models/` - Contains PD-GAN models which were trained on different GPUs using single precision and mixed precision training.
    - `PD_GAN_a100.ipynb/` - Trained on a100 GPU using single precision training.
    - `PD_GAN_a100_MP.ipynb/` - Trained on a100 GPU using mixed precision training.
    - `PD_GAN_v100.ipynb/` - Trained on v100 GPU using single precision training.
    - `PD_GAN_v100_MP.ipynb/` - Trained on v100 GPU using mixed precision training.
  - `Roofline.ipynb` - Roofline model for above 4 models.
  - `make_plots.ipynd` - Contains plots decribing energy, loss, and psnr.
- `Progreesive-Generative-Networks` - Contains optimizations on Progressive Generative Networks
  - `Roofline.ipynb` - Roofline model for Progressive GANs.
  - `plots.ipynb` - contains plots for Progressive GANs decribing energy, loss, and psnr. 
  - `training_single_precison.ipynb` - notebook to train progressive GAN - single precision training. 
  - `training.ipynb` -  notebook to train progressive GAN - mixed precision training. 

## How to run
- To run PD-GAN`
  - Install https://github.com/KumapowerLIU/PD-GAN
  - Download pretrained weights from the above repo for encoder and decoder.
  - In the python notebooks PD_GAN_* run all cells, some libraries are commneted out, use pip install to install them.
  - Change paths to your localhost.
- To run Progressive GANs
  - Install required libraries and install https://github.com/crashmoon/Progressive-Generative-Networks.git
  - Run all cells

## Results

| Model Architecture  | Optimization |
| ------------- | |
| PD-GAN |  |
| Progressive GANs  |  |

## Documentation
- Project report can be found at [docs/Report.pdf](https://github.com/shreya1313/Deep-Learning-Mini-Project/blob/main/docs/Report.pdf)

## Authors
- Saaketh Koundinya : sg7729@nyu.edu
- Jayanth Jayram Sastry : js12891@nyu.edu
