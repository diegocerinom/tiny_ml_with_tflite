# How to start with tiny machine learning with tensorflow lite

This steps are for python code, To you start in Tiny ML with tensorflow, you should used tensorflow lite and install in your Raspberry Pi. you can consult the information in the follow link: https://www.tensorflow.org/lite/guide/python#install_tensorflow_lite_for_python

the library tflite_runtime is available in Python versions 3.5 to 3.9

## Install library tflite_runtime
The reference of the following information is in this link: https://github.com/tensorflow/tensorflow/blob/v2.5.0/tensorflow/lite/g3doc/guide/python.md, you can consult for more information about it.

To install tflite_runtime in Raspberry Pi OS Debian, be used:
<pre>
echo "deb https://packages.cloud.google.com/apt coral-edgetpu-stable main" | sudo tee /etc/apt/sources.list.d/coral-edgetpu.list
<code>curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -</code>
<code>sudo apt-get update</code>
<code>sudo apt-get install python3-tflite-runtime</code>
</pre>

And to install in Ubuntu OS for Raspberry Pi, be used:
```
pip3 install --extra-index-url https://google-coral.github.io/py-repo/ tflite_runtime
```

Also is possible download the file .whl, download in the follow link: https://google-coral.github.io/py-repo/tflite-runtime/


## Import library to Python script

```python
import tflite_runtime.interpreter as tflite

#load model tflite
interpreter = tflite.Interpreter(model_path="path\model.tflite")

```


