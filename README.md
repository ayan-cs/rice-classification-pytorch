# Rice Classification using CNN in PyTorch

### Dataset

The [Original Dataset](https://www.kaggle.com/datasets/muratkokludataset/rice-image-dataset) contains 75000 images of 5 different Rice species. Each of the species has 15000 images each. The basic task is to develop a CNN model to classify a rice grain image into one of these 5 categories correctly.

I have prepared a [Pre-processed Dataset](https://www.kaggle.com/datasets/ayanwap7/rice-image-dataset-train-test-split/code) from the original dataset so as to make it easily usable in PyTorch for preparing the DataLoader using `torchvision.datasets.ImageFolder()` and then using `torch.utils.data.dataloader.DataLoader()`. The directory tree is as follows,
```
Rice_Image_Classification
|
|--- Train
|     |---Arborio (12000 images)
|     |---Basmati (12000 images)
|     |---Ipsala (12000 images)
|     |---Jasmine (12000 images)
|     |---Karacadag (12000 images)
|
|--- Test/Validation
      |---Arborio (3000 images)
      |---Basmati (3000 images)
      |---Ipsala (3000 images)
      |---Jasmine (3000 images)
      |---Karacadag (3000 images)
```

### Config File

You can change the entries in the `config.yaml` file according to the configuration you want the code to run. I have used 1 configuration, which uses **ResNet-18** architecture. For other details, refer to the config file.

### Results

- Performed prediction using Pre-trained ResNet-18. Accuracy on Training data = 17.805 % and that on Validation/Test data = 19.793 %
- Trained ResNet-18 from scratch using Training dataset for 20 epochs. **Train Accuracy = 99.95 % and Validation/Test Accuracy = 99.88 %**

#### Accuracy and Loss Curves

- ResNet-18

![Accuracy Curve](https://drive.google.com/file/d/1STCUbyiluDXe7ghrz6iQlT4H0XQvm371/view?usp=sharing)

![Loss Curve](https://drive.google.com/file/d/1Ou-JMjc19D_TW0_rLzrRSlKIAxD1wydl/view?usp=sharing)

- Rice CNN

![Accuracy Curve](https://drive.google.com/file/d/1tfhL-fwgh_XHjk8lSQB_SOwrSnNA7tum/view?usp=sharing)

![Loss Curve](https://drive.google.com/file/d/1PiI2i7pLNNcU7no57mKy5g67pWC73qso/view?usp=sharing)