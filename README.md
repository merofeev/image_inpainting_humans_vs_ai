# Image Inpainting: Humans vs. AI

The repository contains images used in subjective comparisons of automatic image inpainting methods vs. human artists. The study description is available at [Towards Data Science].

## Repository Structure

The 33 photo patches used in the study are available in [ground_truth directory](ground_truth/). Distorted images given to inpainting mathods and human artists are located in [input directory](input/).

### Automatic Methods
The results of automatic inpainting methods are located in [results/automatic_methods directory](results/automatic_methods/). The file names abide the following pattern: `results/automatic_methods/{TEST_IMAGE_NAME}/{METHOD_NAME}.png`.

Deep learning methods names:
* `deep_image_prior`: Deep Image Prior ([Ulyanov, Vedaldi, and Lempitsky, 2017](https://arxiv.org/abs/1711.10925))
* `globally_and_locally_consistent`: Globally and Locally Consistent Image Completion ([Iizuka, Simo-Serra, and Ishikawa, 2017](http://hi.cs.waseda.ac.jp/~iizuka/projects/completion/en/))
* `high_res_neural_inpainting`: High-Resolution Image Inpainting ([Yang et al., 2017](https://arxiv.org/abs/1611.09969))
* `shift_net`: Shift-Net ([Yan et al., 2018](https://arxiv.org/abs/1801.09392))
* `generative_inpainting_release_*_256`: Generative Image Inpainting With Contextual Attention ([Yu et al., 2018](https://arxiv.org/abs/1801.07892)) — this method appears twice in our results because we tested two versions, each trained on a different data set (ImageNet and Places2)
* `irregular_holes`: Image Inpainting for Irregular Holes Using Partial Convolutions ([Liu et al., 2018](https://arxiv.org/abs/1804.07723))


Conventional inpainting methods:

* `criminisi_*`: Exemplar-Based Image Inpainting ([Criminisi, Pérez, and Toyama, 2004](http://www.irisa.fr/vista/Papers/2004_ip_criminisi.pdf)). The number in the suffix encodes patch size (9 or 13).
* `patch_shift_stats`: Statistics of Patch Offsets for Image Completion ([He and Sun, 2012](http://kaiminghe.com/eccv12/index.html))
* `photoshop_cs_5`: Content-Aware Fill in Adobe Photoshop CS5

### Human Artists

The images drawn by human artists are located in [results/human_artists folder](results/human_artists/). The file names abide the following pattern: `results/human_artists/{TEST_IMAGE_NAME}/artist_{ID}.png`.



[Towards Data Science]: https://towardsdatascience.com/image-inpainting-humans-vs-ai-48fc4bca7ecc
