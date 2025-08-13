#exp 1 solving XOR problem using deep neural network
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
OUTPUT:
<img width="880" height="566" alt="Screenshot 2025-08-06 114041" src="https://github.com/user-attachments/assets/6c69b6f6-7b56-4c7a-a582-2da2256ae55e" />
<img width="590" height="369" alt="Screenshot 2025-08-06 114019" src="https://github.com/user-attachments/assets/6973721a-1f74-4f5a-aab6-372c8f431dda" />

