# ARMnn_Quantize_RPi_32-bits
ARMnn TensorFlow Lite classification for the Raspberry Pi 4

A C++ implementation of ARMnn (ARM Neural Network framework) classification with a TensorFlow Lite model on a Raspberry Pi 4.
Once overclocked to 2000 MHz, your app runs a disappointing 4.6 FPS without any hardware accelerator.

https://arxiv.org/pdf/1712.05877.pdf <br/>
Training set: COCO with 1000 objects<br/>
Size: 224x224 <br/>
Frame rate Mobile_V1 Lite : 4.6 FPS (RPi 4 @ 2000 MHz - 32 bits OS) <br/>
<br/>
Special made for a bare Raspberry Pi see: https://qengineering.eu/install-armnn-on-raspberry-pi-4.html <br/>
<br/>
To extract and run the network in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/ARMnn_Quantize_RPi_32-bits/archive/master.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
tabby.jpeg <br/>
schoolbus.jpg <br/>
grace_hopper.bmp <br/>
Labels.txt <br/>
TestARMnnMobileNetV1_Quant.cpb <br/>
mobilenetv1_quant_tflite.cpp<br/>
model_output_labels_loader.hpp<br/>
 <br/>
Next, choose your model from TensorFlow: https://www.tensorflow.org/lite/guide/hosted_models <br/> 
Download a quantized model, extract the .tflite from the tarball and place it in your *MyDir*. <br/> <br/>
Now your *MyDir* folder may contain: mobilenet_v1_1.0_224_quant.tflite. <br/>
Or: inception_v4_299_quant.tflite. Or both of course. <br/> <br/>
Run TestTensorFlow_Lite.cpb with Code::Blocks.<br/>
Give the .tflite file of your choice and the image to be tested as command line parameter<br/> <br/>
![output image]( https://qengineering.eu/images/Command_line_options.png )<br/> <br/>
Remember, you also need a working OpenCV 4 on your Raspberry. <br/>
Preferably use our installation: https://qengineering.eu/install-opencv-4.3-on-raspberry-pi-4.html <br/>

![output image]( https://qengineering.eu/images/Schoolbus2.png )
