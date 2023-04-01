# -Enhancement-of-Images-Captured-in-Low-Light-Conditions
Videos captured in low-light conditions frequently have poor brightness, low contrast, a limited
range of grayscale, color distortion, jitter, and substantial noise, which negatively affects the
subjective visual experience of human eyes and severely restricts the effectiveness of high-level

machine vision techniques. there are several architectures proposed in a low light video en-
hancement, Zero-DCE (DCE-Net) is one of the existing architectures, given an input image, the

Deep Curve Estimation Network (DCE-Net) is designed to estimate a set of Light-Enhancement
curves (LE-curves) that fit the input image the best. The framework then applies the curves

iteratively to map each RGB channel’s pixels to create the final improved image. It continu-
ously improves and uses the image with the highest exposure as its ground truth until successful

results are reached. Given that Zero-DCE is an unsupervised technique, The noise in the en-
hanced image prevents it from extracting local and global features. Therefore, we propose an

architecture namely Low Light Video Enhancement(LLVE-Net), in which we are using percep-
tual loss addition to the loss functions used in Zero-DCE. The enhanced image in DCE-Net does

not extract local and global features accurately and the enhanced image consists of high-level
noise, to extract local and global features accurately we are using a cascading technique where
the enhanced image is cascaded back to LLVE-Net so that it extracts those features that the
model has not previously learned. So by cascading we can extract nearly all the local and global

features and make our model more robust, by doing so our model consistently outperforms Zero-
DCE.
