# Deep Learning Specialization - Course 1 Formula Sheet

## 1. Linear Forward Propagation

```text
Z = W × A + b
```

Where:

- `W` = weights
- `A` = activations from previous layer
- `b` = bias
- `Z` = output before activation

---

## 2. Sigmoid Activation

```text
A = 1 / (1 + e⁻ᶻ)
```

Example:

```text
If Z = 2

A = 1 / (1 + e⁻²)
```

---

## 3. ReLU Activation

```text
A = max(0, Z)
```

Examples:

```text
Z = 5  →  A = 5

Z = -3 →  A = 0
```

---

## 4. Binary Cross Entropy Cost

```text
Cost = -(1/m) × Σ [ Y × log(AL) + (1-Y) × log(1-AL) ]
```

Where:

- `m` = number of training examples
- `Y` = actual value
- `AL` = prediction of last layer

---

## 5. Derivative of Sigmoid

```text
sigmoid'(Z) = sigmoid(Z) × (1 - sigmoid(Z))
```

Since:

```text
A = sigmoid(Z)
```

We usually write:

```text
dZ = dA × A × (1 - A)
```

---

## 6. Derivative of ReLU

```text
If Z > 0:

dZ = dA
```

```text
If Z ≤ 0:

dZ = 0
```

---

## 7. Linear Backward Propagation

For:

```text
Z = W × A + b
```

### Weight Gradient

```text
dW = (1/m) × dZ × Aᵀ
```

### Bias Gradient

```text
db = (1/m) × sum(dZ)
```

### Previous Activation Gradient

```text
dA_prev = Wᵀ × dZ
```

---

## 8. Initial Gradient for Backpropagation

```text
dAL = - [ (Y / AL) - ((1-Y)/(1-AL)) ]
```

Used only at the output layer.

---

## 9. Gradient Descent Update

### Update Weights

```text
W = W - learning_rate × dW
```

### Update Biases

```text
b = b - learning_rate × db
```

---

# Only 6 Formulas To Remember

### 1.

```text
Z = W × A + b
```

### 2.

```text
A = 1 / (1 + e⁻ᶻ)
```

### 3.

```text
A = max(0, Z)
```

### 4.

```text
dZ = dA × A × (1 - A)
```

### 5.

```text
dW = (1/m) × dZ × Aᵀ
```

### 6.

```text
W = W - learning_rate × dW
```

---

## Course 1 Goal

Understand:

- Forward Propagation
- ReLU
- Sigmoid
- Cost Function
- Backpropagation
- Gradient Descent

These concepts form the foundation for all later Deep Learning Specialization courses.