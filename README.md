# Captcha Decoder Using Deep Learning
Captcha Decoder is a project that uses deep learning techniques to automatically decipher captcha images. Captchas are widely used to prevent bots from accessing certain online services, but they can be challenging for machines to read accurately. This project aims to develop an accurate and efficient system to automate the captcha-solving process.

### Technologies Used
- Python 3.x
- TensorFlow (or TensorFlow-GPU for GPU support)
- Keras
- OpenCV
- Numpy

### Solving Process
1. download the captcha image from the provided source. The standard size for this particular example is 200x50 pixels. The captcha images look like the following one:
   
![Sample Captcha](https://imgtr.ee/images/2023/07/15/c2306e3b07e5b30ce2bff4bebccc6338.png)

2. Preprocess the images:
- Convert the image into its binary representation (which means turning all pixels to either black or white). This makes further processing way easier with an acceptable loss of information. (In the provided datasets all images are already black & white)
- Divide the captcha into the single letters that compose it. Considered captchas had 6 letters.
- Normalized obtained letters into a 32x32 pixels format in which letters are centered. This consistent format makes the Neural Network perform way better.
3. Feed groups of letters into the trained Neural Network.
4. Solved!

### Neural Network Architecture
The following image is a representation of the Neural Network that was used. This architecture was designed for a wider range of possible letters but it works pretty good on smaller ranges too.

![CNN Model](https://imgtr.ee/images/2023/07/15/a5f96879e05c3486611bbd7204aa879f.png)

### Performances
- The training of the Neural Network takes a small amount of time around ~7 minutes.
- It takes it about 12 seconds to solve 50 captchas, including download and preprocessing.
- On average, the trained Neural Network achieved a mean success rate of ~86%, peaking at 83%.
