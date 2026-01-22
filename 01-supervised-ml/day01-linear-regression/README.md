# Machine Learning – Important Notes (Concise)

> 📌 **Focused, exam + interview + revision ready notes**
> Only **important concepts** kept, noise removed.

---

## 1. Learning Types

### Supervised Learning

* Learns from **labeled data (x, y)**
* Learns by comparing predictions with **right answers**
* Examples:

  * Linear Regression
  * Logistic Regression

### Unsupervised Learning

* Data has **inputs x only**, no labels y
* Goal → **find structure in data**

#### Types of Unsupervised Learning

* **Clustering** → group similar data points
* **Anomaly Detection** → find unusual / rare points
* **Dimensionality Reduction** → compress data

---

## 2. Linear Regression (Core Intuition)

### Important Note ⚠️

**Linear ≠ straight line**

Linear means:

* Linear **with respect to parameters (w, b)**

Model:

```
f(x) = wx + b
```

* **w** → slope / weight
* **b** → bias / shift

By tuning `w` and `b`, we get the **best-fit line**.

---

## 3. Cost Function

* Cost function = **error measure**
* Tells how bad current parameters are
* Goal → **minimize cost**

---

## 4. Gradient Descent (Very Important ⭐)

### Core Idea

**Gradient Descent = downhill movement**

* Cost surface = hill
* Height = error
* Minimum = best (w, b)

### Gradient

* Gradient = **uphill direction**
* To go downhill → move in **negative gradient** direction

### Update Rule

```
w = w − α * ∂J/∂w
```

* `α (alpha)` → learning rate (step size)
* `∂J/∂w` → slope of cost function

### Learning Rate

* Too large → overshoot
* Too small → slow convergence

---

## 5. Types of Gradient Descent

### Batch Gradient Descent

* Uses **entire dataset** per update
* ✅ Stable, smooth convergence
* ❌ Slow for large datasets

### Mini-batch Gradient Descent ✅

* Uses small batches
* Best trade-off between **speed & stability**

---

## 6. Multiple Features (Vector Form)

* Feature vector:

```
x = [x₁, x₂, ..., xₙ]
```

* Parameters:

```
w = [w₁, w₂, ..., wₙ]
```

* Prediction:

```
f(x) = w · x + b
```

### Vectorization ⭐

* Faster computation
* Cleaner math
* Gradient Descent remains same → **more w’s only**

---

## 7. Normal Equation

* Direct solution (no iterations)
* Computationally expensive
* Not suitable for large datasets

---

## 8. Feature Scaling (Very Important ⭐⭐)

### Problem (Tall & Skinny Contours)

* Features have very different ranges
* Gradient Descent zig-zags → slow convergence

### Solution

**Normalize features**

#### Techniques

* Divide by max value
* Mean normalization
* Z-score normalization

👉 Result: **fast & stable convergence**

---

## 9. Checking Convergence

### Learning Curve

* Cost should decrease every iteration
* Flat curve → convergence reached

### Automatic Convergence Test

* Stop if cost decrease < ε (epsilon)

---

## 10. Feature Engineering (Very Important ⭐⭐)

* Create better features using intuition
* Example:

  * Depth + Width → Area

👉 Better features = better performance

---

## 11. Polynomial Regression

### Important Clarification ⚠️

**Polynomial Regression ≠ Non-linear model**

* Still linear in parameters
* Uses polynomial features

---

## 🔁 Final Revision Snapshot

* Supervised → labels
* Unsupervised → structure
* Linear ≠ straight line
* w = slope, b = shift
* Cost function = error
* Gradient = uphill direction
* Minus sign = downhill move
* Alpha = step size
* Batch GD = stable but slow
* Mini-batch = practical choice
* Vectorization = speed + clarity
* Feature scaling → fast convergence ⭐
* Feature engineering → performance boost ⭐
* Polynomial regression ≠ non-linear model ⭐
