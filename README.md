<!-- PROJECT LOGO -->
<br />
<p align="center">
    <img src="./images/DeepLIIF_logo.png" width="50%">
    <h3 align="center"><strong>Deep-Learning Inferred Multiplex Immunofluorescence for IHC Image Quantification</strong></h3>
    <p align="center">
    <a href="https://doi.org/10.1101/2021.05.01.442219">Read Link</a>
    |
    <a href="https://deepliif.org/">AWS Cloud Deployment</a>
    |
    <a href="https://colab.research.google.com/drive/12zFfL7rDAtXfzBwArh9hb0jvA38L_ODK?usp=sharing">Google CoLab Demo</a>
    |
    <a href="#docker-file">Docker</a>
    |
    <a href="https://github.com/nadeemlab/DeepLIIF/issues">Report Bug</a>
    |
    <a href="https://github.com/nadeemlab/DeepLIIF/issues">Request Feature</a>
  </p>
</p>

*Reporting biomarkers assessed by routine immunohistochemical (IHC) staining of tissue is broadly used in diagnostic 
pathology laboratories for patient care. To date, clinical reporting is predominantly qualitative or semi-quantitative. 
By creating a multitask deep learning framework referred to as DeepLIIF, we present a single-step solution to stain 
deconvolution/separation, cell segmentation, and quantitative single-cell IHC scoring. Leveraging a unique de novo 
dataset of co-registered IHC and multiplex immunofluorescence (mpIF) staining of the same slides, we segment and 
translate low-cost and prevalent IHC slides to more expensive-yet-informative mpIF images, while simultaneously 
providing the essential ground truth for the superimposed brightfield IHC channels. Moreover, a new nuclear-envelop 
stain, LAP2beta, with high (>95%) cell coverage is introduced to improve cell delineation/segmentation and protein 
expression quantification on IHC slides. By simultaneously translating input IHC images to clean/separated mpIF channels 
and performing cell segmentation/classification, we show that our model trained on clean IHC Ki67 data can generalize to 
more noisy and artifact-ridden images as well as other nuclear and non-nuclear markers such as CD3, CD8, BCL2, BCL6, 
MYC, MUM1, CD10, and TP53. We thoroughly evaluate our method on publicly available benchmark datasets as well as against 
pathologists' semi-quantitative scoring.*

© This code is made available for non-commercial academic purposes.

![overview_image](./images/overview.png)**Figure 1**. *Overview of DeepLIIF pipeline and sample input IHCs (different 
brown/DAB markers -- BCL2, BCL6, CD10, CD3/CD8, Ki67) with corresponding DeepLIIF-generated hematoxylin/mpIF modalities 
and classified (positive (red) and negative (blue) cell) segmentation masks. (a) Overview of DeepLIIF. Given an IHC 
input, our multitask deep learning framework simultaneously infers corresponding Hematoxylin channel, mpIF DAPI, mpIF 
protein expression (Ki67, CD3, CD8, etc.), and the positive/negative protein cell segmentation, baking explainability 
and interpretability into the model itself rather than relying on coarse activation/attention maps. In the segmentation 
mask, the red cells denote cells with positive protein expression (brown/DAB cells in the input IHC), whereas blue cells 
represent negative cells (blue cells in the input IHC). (b) Example DeepLIIF-generated hematoxylin/mpIF modalities and 
segmentation masks for different IHC markers. DeepLIIF, trained on clean IHC Ki67 nuclear marker images, can generalize 
to noisier as well as other IHC nuclear/cytoplasmic marker images.*

## Issues
Please report all issues on the public forum.


## License
© [Nadeem Lab](https://nadeemlab.org/) - DeepLIIF code is distributed under **Apache 2.0 with Commons Clause** license, 
and is available for non-commercial academic purposes. 

## Acknowledgments
* This code is inspired by [CycleGAN and pix2pix in PyTorch](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix).

## Reference
If you find our work useful in your research or if you use parts of this code, please cite our paper:
```
@article{ghahremani2022deepliif,
  title={Deep Learning-Inferred Multiplex ImmunoFluorescence for IHC Image Quantification},
  author={Ghahremani, Parmida and Li, Yanyun and Kaufman, Arie and Vanguri, Rami and Greenwald, Noah and Angelo, Michael and Hollmann, Travis J and Nadeem, Saad},
  journal={Nature Machine Intelligence},
  year={2022}
}
```
