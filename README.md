# Multi-Channel-dino

An adaptation of [Facebookresearch's](https://github.com/facebookresearch) [dino algorithm](https://github.com/facebookresearch/dino) to 5 channels, easily adaptable to any number of channels (rather than just RGB).

This work was done with [Cell Painting](https://www.nature.com/articles/nprot.2016.105) 5-channel data in mind, but could be useful for any other medical or biological imaging modalities with greater or fewer than 3 channels.

# Note about this work

While a simple adapation, I am sure many people working with multi-channel data such as fluorescent cell images have struggled adapting many existing frameworks with 3-channel (typically RGB) implementations. For [dino](https://arxiv.org/abs/2104.14294) there are a number of augmentation steps applied to each channel in training. Most augmentation toolboxes do no work well for multi-channel (>3) images. RGB is [overwhelmingly](https://image-net.org/) common for datasets in computer vision beyond grayscale.

The function "NaturalImageDataset" is the main contribution here. While fairly 'hard-coded', it is a practical solution to the lack of support for multi-channel augmentations. Please let me know if there are more elegant implementations.
