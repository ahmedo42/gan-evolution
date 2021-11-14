# GAN Normalization Evolution
This repo demonstrates the effect of different normalization techniques on training GANs on the MNIST dataset.

By running the notebook on Kaggle Kernels or Google Colab with GPU the following results should be reproduced without 
installing any packages.

All models were trained for 25 epochs and noise dimensionality of Z=64.

<ul>
    <li>
    <p> Linear Layers Without BatchNorm (didn't converge after 25 epochs)</p>
    <img src="./results/linear_final.png">
    </li>
    <li>
    <p> Linear Layers + 1D BatchNorm</p>
    <img src="./results/linear_batchnorm_3000.png">
    <img src="./results/linear_batchnorm_done.png">
    </li>
    <li>
    <p> CNN + 2D BatchNorm</p>
    <img src="./results/cnn_batchnorm_3000.png">
    <img src="./results/cnn_batchnorm_done.png">
    </li>
    <li>
    <p> CNN + Pytorch's spectral_norm</p>
    <img src="./results/spectral_3000.png">
    <img src="./results/spectral_done.png">
    </li>
    <li>
    <p> CNN + Implemented spectral norm</p>
    <img src="./results/custom_3000.png">
    <img src="./results/custom_done.png">
    </li>
</ul>

### References
- [Original GAN Paper](https://arxiv.org/abs/1406.2661)
- [DCGAN Paper](https://arxiv.org/pdf/1511.06434)
- [Spectral Normalization Paper](https://arxiv.org/abs/1802.05957)
- [Coursera GAN Specialization](https://github.com/amanchadha/coursera-gan-specialization)
- [Spectral Norm Reference Implementation](https://github.com/christiancosgrove/pytorch-spectral-normalization-gan)
