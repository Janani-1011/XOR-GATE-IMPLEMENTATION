### EX NO : 08
### DATE  : 16/05/2022
# <p align="center"> XOR GATE IMPLEMENTATION </p>
## AIM:
   To implement multi layer artificial neural network using back propagation algorithm.
## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## RELATED THEORY CONCEPTS:
The XOR gate stands for the Exclusive-OR gate. This gate is a special type of gate used in different types of computational circuits. Apart from the AND, OR, NOT, NAND, and NOR gate, there are two special gates, i.e., Ex-OR and Ex-NOR. This neural network will deal with the XOR logic problem. An XOR (exclusive OR gate) is a digital logic gate that gives a true output only when both its inputs differ from each other.

## ALGORITHM:
1. Import the required libraries.
2. Create the training dataset.
3. Create the neural network model with one hidden layer.
4. Train the model with training data.
5. Now test the model with testing data.

## PROGRAM:
```
/*
Program to implement XOR Logic Gate.
Developed by   : JANANI D
RegisterNumber : 212220040056
*/
import numpy as np
from keras.models import Sequential
from keras.layers.core import Dense

training_data=np.array([[0,0],[0,1],[1,0],[1,1]],"float32")
target_data=np.array([[0],[1],[1],[0]],"float32")

model=Sequential()
model.add(Dense(16,input_dim=2,activation='relu'))
model.add(Dense(1,activation='sigmoid'))
model.compile(loss='mean_squared_error',
                    optimizer='adam',
                    metrics=['binary_accuracy'])
model.fit(training_data,target_data,epochs=1000)
scores=model.evaluate(training_data,target_data)

print("\n%s: %.2f%%" % (model.metrics_names[1],scores[1]*100))
print(model.predict(training_data).round())
```

## OUTPUT:
![XOR](https://user-images.githubusercontent.com/86832944/169465430-897846bc-c89b-4981-b3bf-86302dafc15e.png)



## RESULT:
Thus the python program successully implemented XOR logic gate.
