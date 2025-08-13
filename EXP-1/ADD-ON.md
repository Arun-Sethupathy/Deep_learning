#exp1 add on
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
OUTPUT:
<img width="622" height="456" alt="Screenshot 2025-08-06 114108" src="https://github.com/user-attachments/assets/25cae25d-8434-492e-82bc-554fa6081eb8" />
<img width="579" height="334" alt="Screenshot 2025-08-06 114058" src="https://github.com/user-attachments/assets/df084aca-113e-48e4-b7f4-e68389a70323" />
