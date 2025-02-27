# RandomVariableSimulation

This repository implements and analyzes methods for simulating random variables, focusing on the acceptance-rejection method. Tasks include proving correctness, studying the complexity of simulating a standard normal distribution from a symmetric exponential distribution, and comparing it with the Box-Muller method.

## Tasks

### 1. Correctness Proof

- Prove that the implemented procedure correctly simulates the distribution given in the task.

### 2. Acceptance-Rejection Method

- Study the complexity of simulating a standard normal distribution from a symmetric exponential distribution with the density:

  \[
  g(x) = \frac{\alpha}{2} e^{-\alpha |x|}
  \]

  where \( \alpha \) is a parameter.

### 3. Comparison with Box-Muller Method

- Compare the complexity of this method with the Box-Muller method for simulating a standard normal distribution:
  1. Simulate \( U_1, U_2 \sim \mathcal{U}[0, 1] \).
  2. Compute:
     \[
     X_1 = \sqrt{-2 \log U_1} \cos(2\pi U_2)
     \]
     \[     X_2 = \sqrt{-2 \log U_1} \sin(2\pi U_2)     \]

- Use the `microbenchmark` package to compare the computational complexity of the two methods.

## Example Task

Evaluate the complexity of simulating a standard normal distribution using the following density:

\[
g(x) = \frac{\alpha}{2} e^{-\alpha |x|}
\]

where \( \alpha \) is a parameter, and demonstrate that:

\[
\frac{f(x)}{g(x)} \leq \sqrt{\frac{2}{\pi}} \frac{1}{\alpha} e^{\alpha^2 / 2}
\]

where \( f(x) \) is the density of the standard normal distribution.
