# Rice Classification using CNN in PyTorch

### Dataset

The Original Dataset contains 75000 images of 5 different Rice species. Each of the species has 15000 images each. The basic task is to develop a CNN model to classify a rice grain image into one of these 5 categories correctly.

I have prepared a Pre-processed Dataset from the original dataset so as to make it easily usable in PyTorch for preparing the DataLoader using `torchvision.datasets.ImageFolder()` and then using `torch.utils.data.dataloader.DataLoader()`. The directory tree is as follows,
```
Rice_Image_Classification
|
|--- Train
|     |---Arborio
|     |---Basmati
|     |---Ipsala
|     |---Jasmine
|     |---Karacadag
|
|--- Test/Validation
|     |---Arborio
|     |---Basmati
|     |---Ipsala
      |---Jasmine
      |---Karacadag
```
