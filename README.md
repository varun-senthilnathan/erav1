
# ERA V1 Session 5 Assignment

This folder contains my submission for the ERA-V1 Session 5 assignment. The code has been organised into the following files:

## model.py
This file contains the code that created the Neural Network. It contains two networks ```Net``` and ```Net2```. A sample usage has been mentioned below

```
from model import Net

use_cuda = torch.cuda.is_available()
device = torch.device("cuda" if use_cuda else "cpu")
model = Net().to(device)
summary(model, input_size=(1, 28, 28))
```

or

```
from model import Net2

use_cuda = torch.cuda.is_available()
device = torch.device("cuda" if use_cuda else "cpu")
model = Net2().to(device)
summary(model, input_size=(1, 28, 28))
```

## utils.py

This file contains the commonly used functions for training and testing the networks.

The ```train``` method can be called like :
```
train_acc, train_losses = train(model, device, train_loader, optimizer, criterion, train_acc, train_losses)
```

and the test function like :
```
test_acc, test_losses = test(model, device, test_loader, criterion, test_acc, test_losses)
  ```

## S5.ipynb
This file contains the code that is executed for every run. This file contains a sample run using the above files.