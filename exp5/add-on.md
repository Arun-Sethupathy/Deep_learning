from keras.models import Sequential 
from keras.layers import Embedding, GRU, Dense 
model = Sequential([ 
Embedding(10000, 32, input_length=100), 
GRU(100), 
Dense(1, activation='sigmoid') 
]) 
model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy']) 
model.fit(X_train, y_train, epochs=5, batch_size=64, validation_split=0.2) 

output:

<img width="918" height="220" alt="Screenshot 2025-09-03 110856" src="https://github.com/user-attachments/assets/7dffa069-530f-48ef-b1ff-e0c435e08b03" />

