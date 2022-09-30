# PENG TinyML Final

## File Description
【**Model_Training_Design_Repo**】: This file contains the 5 layer CNN model with focal loss using Pytorch frameworks. 

【**C_Sourch_Code_Repo**】: This file contains the C code generated by STM32CubeMX.

【**Quant_fft_model**】: This file Contains a quanzied CNN model with 2 channel input (time and frequency). 

【**Trained_Model_Weights**】: The training model weights file in onnx.

【**Validation**】:File you can used to test our model once you download the C code your board.

【**requirements.txt**】: The required version you need to install.

## How to run the code
1. Connect your STM 32 using `usb2micro usb cable` to your computer and double-check the `port number` via the `Device Manager`.
2. Open `\PENG\C_Sourch_Code_Repo\MDK_ARM\Peng_model.uvprojx` in KeiluVision5, and download it on your STM32.
3. Run following code in your terminal.

```python
  pip install requirements.txt
```

4. Open `Validation` as a project in you python IDE (eg: Pycharm) and **change** `com4` in `validation.py` to the one you checked in the first step.
5. Run the `validation.py` and press reset button.

## What's new about our model
1. We use `train_validation_split` when we train the model
2. We change loss function to `Focal Loss`
3. We process the original data and cange 1 channel time data to `2 channel input data (time + frequence)`
4. We use `static quantization` in pytorch to quant final model
