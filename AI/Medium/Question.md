# Level 3 Task: Building a Visual Neural Decision Network 🧠⚡

Welcome back! Now that you have mastered basic text logic and decision routing, it is time to take a peek inside how **Deep Learning and Neural Networks** make decisions. 

Instead of jumping straight into heavy frameworks like PyTorch or TensorFlow, you are going to build a **simulated mini-neural network from scratch** using pure Python. You will create a visual representation of how a network takes multiple inputs, multiplies them by "weights", sums them up, and uses an activation function to trigger a final decision!

---

## 🧠 Understanding the Concept

In a real neural network:
1. **Inputs** ($x$): Raw data features (e.g., student attendance, study hours).
2. **Weights** ($w$): Importance values assigned to each input (learned during training).
3. **Bias** ($b$): A baseline threshold that shifts the decision boundary.
4. **Activation Function**: A mathematical gate (like a step function or Sigmoid) that turns the final sum into a clear output (e.g., 0 or 1).

Your goal is to build a text-based visual simulator that logs every step of this forward pass so you can literally *see* how the network thinks.

---

## 📝 The  Task

### Objective
Write a Python program that simulates a single-layer Neural Network (a Perceptron) to predict whether a student should pass an exam based on two inputs: **Study Hours** and **Attendance Rate**.

### Requirements
1. **Define the Network Parameters:**
   * Inputs: `study_hours` (normalized between 0 and 1) and `attendance` (normalized between 0 and 1).
   * Weights: `w1 = 3.5`, `w2 = 2.0`
   * Bias: `bias = -3.0`
2. **The Forward Pass Function:**
   * Calculate the weighted sum: $\text{sum} = (x_1 \times w_1) + (x_2 \times w_2) + \text{bias}$.
3. **The Activation Function (The Threshold Gate):**
   * Write an activation function (like a Step Function): if the weighted sum $\ge 0$, output `1` (Pass); otherwise, output `0` (Fail).
4. **Visual Console Logger:**
   * Print out a clean, step-by-step visual trace showing the math at each node (Input $\rightarrow$ Weight Multiplication $\rightarrow$ Summation $\rightarrow$ Activation Decision).

# Resources:
Youtube video link : https://www.youtube.com/watch?v=EYeF2e2IKEo 


documentation : https://victorzhou.com/blog/intro-to-neural-networks/
