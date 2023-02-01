# MNIST-Classification

## Description
MNIST is a collection of handwritten digits ranging from the number 0 to 9. It has a training set of 60,000 images, and 10,000 test images that are classified into corresponding categories or labels. Multilayer Perceptrons (MLP) model has been deployed using Keras. 

Batch size of 128, Hidden units of 256 and Dropout of 0.45 with Epochs of 20 to achieve 98.2% accuracy. 

## Libraries 
* Keras
* numpy
* pandas
* matplotlib

## Tool
* Google Colab

## Network parameters

```python
batch_size = 128
hidden_units = 256
dropout = 0.45
```

## Model Arhitecture
```python
# model is a 3-layer MLP with ReLU and dropout after each layer
model = Sequential()
model.add(Dense(hidden_units,activation="relu",input_dim=input_size))
model.add(Dropout(dropout))
model.add(Dense(hidden_units,activation="relu"))
model.add(Dropout(dropout))
model.add(Dense(num_labels))
model.add(Activation('softmax'))
```

## Model Compile
```python
model.compile(loss='categorical_crossentropy',
              optimizer='adam',
              metrics=['accuracy'])
```

## Training the model
```python
model.fit(x_train,y_train,epochs=20, batch_size = batch_size)
```
