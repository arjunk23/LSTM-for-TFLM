# LSTM-for-TFLM
Patch which includes all changes necessary in order for LSTM to compile, not run, on TFLM.

Has changes in header files to include registration of function as well as changes within LSTM and other files in TFLM to achieve compilation on HiFi 4 DSPs
# To apply patch
$ git clone https://github.com/tensorflow/tensorflow.git

$ cd tensorflow

$ git checkout 285b5fa15405c5e2c084080f52a1818be8648079

$ git apply 0001-lstm-compile-lstm-for-tflm.patch
$ make -f tensorflow/lite/micro/tools/make/Makefile test_micro_speech_test


