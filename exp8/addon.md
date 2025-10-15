import numpy as np
from keras.datasets import fashion_mnist
(X_train, _), (_, _) = fashion_mnist.load_data()
X_train = (X_train.astype(np.float32) - 127.5) / 127.5
X_train = np.expand_dims(X_train, axis=-1)

output:
<img width="807" height="135" alt="Screenshot 2025-10-15 093704" src="https://github.com/user-attachments/assets/66e7d45c-9323-4b96-8d50-7947f47640e6" />
