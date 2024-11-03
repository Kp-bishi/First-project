**Problem Statement**
A heat engine currently operating at 55% efficiency. I aim to increase this efficiency to 65%. Efficiency (η\etaη) of a heat engine .

**Python Code**
import matplotlib.pyplot as plt
import numpy as np

# Parameters
current_efficiency = 0.55  # 55%
target_efficiency = 0.65   # 65%
heat_input = 1000          # Initial heat input (Q_input) in joules

# Calculate the initial work output based on current efficiency
work_output_initial = current_efficiency * heat_input

# Generate data for work output range
work_outputs = np.linspace(work_output_initial, heat_input, 100)  # Possible work output values
efficiencies = work_outputs / heat_input  # Calculate efficiencies for each work output

# Plot the efficiency as a function of work output
plt.figure(figsize=(10, 6))
plt.plot(work_outputs, efficiencies, label="Efficiency vs. Work Output", color='b')

# Mark current and target efficiency levels
plt.axhline(y=current_efficiency, color='r', linestyle='--', label="Current Efficiency (55%)")
plt.axhline(y=target_efficiency, color='g', linestyle='--', label="Target Efficiency (65%)")

# Plot labels and title
plt.xlabel("Work Output (Joules)")
plt.ylabel("Efficiency (%)")
plt.title("Efficiency as a Function of Work Output")
plt.legend()
plt.grid(True)

# Show the plot
plt.show()


**Result :
Initial Work Output (W_initial): 550.00 J
Required Work Output (W_target): 650.00 J
Work Increase Needed: 100.00 J
Reduced Heat Input for Target Efficiency: 846.15 J**
