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

