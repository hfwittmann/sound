Audio compression via images


In this post we will use an image compression technique to compress audio signals. We start with a few highlights, screenshots and audio snippets.

We demonstrate an image-based compression of audio files. To convert sound into images we use Short-time Fourier transform (STFT) and its inverse, both from the python audio package librosa. STFT yields a complex two dimensional matrix which can be inverted to obtain the original audio signal. This complex STFT “image” can be separated two “images”, into real and complex parts. These can be compressed and subsequently inverted to yield the compressed audio image.

The SVD method is not as efficient as SOTA techniques such as JPEG. The point here is to move the compression from one domain to another, ie from audio to images. It might however be worthwhile, and could turn into another post, to compare the efficiency of

SOTA Audio compression vs
STFT -> SOTA Image compression > Inverse SFTF
The bird’s eye view of the presented material is as follows:

Intro image compression demo : Compress colored photo image by splitting it into RGB (red, green and brown) images
Audio compression demo: Compress audio by converting the sound into an RC (real and imaginary) image and then convert the compressed RC image back again
This post is a summary of a notebook. The notebook itself is interactive, while this post here intends to to present a bird’s eye view. The notebook can be run interactively on Colab, without the need to install anything, the link is here: https://colab.research.google.com/github/hfwittmann/sound/blob/master/Compress_audio_via_images.ipynb

Hint : The easiest way to use the Colab notebook is to

run all the cells (via >Runtime>Run all)
then scroll down to the images and select the values you want (for the name and the number of components)
1.	Piczak KJ. ESC-50: Dataset for Environmental Sound Classification. ESC-50: Dataset for Environmental Sound Classification. https://github.com/karoldvl/ESC-50/. Published March 1, 2020. Accessed March 1, 2020.
2.	Baumann T. Image Compression with Singular Value Decomposition. https://timbaumann.info/. https://timbaumann.info/. Published March 1, 2020. Accessed March 1, 2020.