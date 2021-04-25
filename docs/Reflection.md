# Reflection

## Problems I faced

### Resizing the images

Resizing the images is mandatory, because the model input has to be consistent. All the images taken by the MyNaturewatch camera are of the same dimension, so I downsized to a resolution congruent to the original dimension. I also webscraped some images, and sometimes they were portrait so I had to discard those (resizing them would distort the image too much). The problem was that TensorFlow's reshape layer was not working like it was supposed to. I spend a couple of days scratching my head, but just gave up and used OpenCV's image `resize` method.

### Python OpenCV

Python OpenCV wasn't working like it was supposed to. I think it was because I compiled it with CUDA incorrectly, or it was a conda issue and I wasn't installing it correctly. This was an unessecary issue that frustrated me, because C++ errors are not helpful. I just reinstalled the whole thing, keeping in mind not to disturb my TensorFlow + CUDA setup.

## What I liked

This was my first time building a real model by myself, from start to finish. There was some feeling of accomplishment at the end, because I solved a problem I was facing using machine learning.

## Improvements

### Transfer Learning

Using a pre-built model would hopefully increase the test accuracy / decrease loss, but it is not as fun as building your own model. Denfintely doable, though.

## What I learned

- TensorFlow API
- Python SCP/SSH APIs