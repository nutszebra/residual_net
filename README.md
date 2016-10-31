# What's this
Implementation of Residual Networks (ResNet) by chainer  

# Dependencies

    git clone https://github.com/nutszebra/residual_net.git
    cd residual_net
    git clone https://github.com/nutszebra/trainer.git

# How to run
    python main.py -p ./ -g 0 


# Details about my implementation
All hyperparameters and network architecture are the same as in [[1]][Paper] except for data-augmentation.  
* Data augmentation  
Train: Pictures are randomly resized in the range of [28, 36], then 26x26 patches are extracted randomly and are normalized locally. Horizontal flipping is applied with 0.5 probability.  
Test: Pictures are randomly resized to 32x32, then they are normalized locally. Single image test is used to calculate total accuracy.  

# Cifar10 result

| network              | depth | total accuracy (%) |
|:---------------------|-------|-------------------:|
| ResNet [[1]][Paper]  | 164    | 94.54             |
| my implementation    | 164    | soon              |
| ResNet [[1]][Paper]  | 1001   | 95.08             |


# References
Identity Mappings in Deep Residual Networks [[1]][Paper]

[paper]: https://arxiv.org/abs/1603.05027 "Paper"
