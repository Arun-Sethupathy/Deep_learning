code:
from keras.models import Sequential
from keras.layers import Dense
import numpy as np
import matplotlib.pyplot as plt

X = np.array([[0,0], [0,1], [1,0], [1,1]])
Y = np.array([[0], [1], [1], [0]])

model = Sequential()
model.add(Dense(4, input_dim=2, activation='relu'))
model.add(Dense(1, activation='sigmoid'))
model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])

history = model.fit(X, Y, epochs=1000, verbose=0)

loss, acc = model.evaluate(X, Y)
print("Accuracy:", acc)

print("Predictions:", model.predict(X))

plt.plot(history.history['loss'])
plt.title('Model Loss')
plt.xlabel('Epoch')
plt.ylabel('Loss')
plt.grid(True)
plt.show()

output:
<img width="880" height="566" alt="Screenshot 2025-08-06 114041" src="https://github.com/user-attachments/assets/fcb7ff2c-b391-4687-adab-54465085c4d7" />
<img width="590" height="369" alt="Screenshot 2025-08-06 114019" src="https://github.com/user-attachments/assets/ab62bf4f-2ed3-49e4-8ac4-983c7140e976" />




add on:

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import Perceptron
X = np.array([[0,0],[0,1],[1,0],[1,1]])
y = np.array([0,1,1,0])
clf = Perceptron(tol=1e-3, random_state=0)

clf.fit(X, y)
print("Predictions:", clf.predict(X))

for i in range(len(X)):
if y[i] == 0:
plt.scatter(X[i][0], X[i][1], color='red')
else:
plt.scatter(X[i][0], X[i][1], color='blue')

x_values = [0, 1]
y_values = -(clf.coef_[0][0]*np.array(x_values) + clf.intercept_)/clf.coef_[0][1]
plt.plot(x_values, y_values)
plt.title('Perceptron Decision Boundary for XOR')
plt.show()

output:
<img width="622" height="456" alt="Screenshot 2025-08-06 114108" src="https://github.com/user-attachments/assets/67c68430-2142-48a9-8089-cded1f1b8dfe" />
<img width="579" height="334" alt="Screenshot 2025-08-06 114058" src="https://github.com/user-attachments/assets/c229c95c-71d8-4bb0-b697-9daa3071775f" />

