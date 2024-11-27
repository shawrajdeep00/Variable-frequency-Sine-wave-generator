# Variable Frequency Sine Wave Generator

This repository provides a MATLAB implementation for generating and visualizing sine waves with varying frequencies. The code supports both **linear** and **logarithmic** frequency scaling, offering flexibility for various use cases such as signal processing, waveform analysis, and educational demonstrations.

## Features

### 1. Custom Frequency Range
- Define your starting and ending frequencies for precise control over the frequency range.
- Example:
  - Starting Frequency: `10 kHz`
  - Ending Frequency: `10 MHz`

### 2. Linear and Logarithmic Scaling
- **Linear Scaling**: Frequencies are generated at evenly spaced intervals between the starting and ending values.
- **Logarithmic Scaling**: Frequencies are spaced logarithmically, making it ideal for applications where exponential frequency growth is relevant.

### 3. Dynamic Sine Wave Visualization
- Real-time plotting of sine waves for each frequency point in the specified range.
- Adjustable parameters for the number of frequency points and time intervals.

## How It Works
The code generates sine waves using the following steps:

1. Define the range of frequencies (`f1` for start and `f2` for end).
2. Choose a scaling method (linear or logarithmic).
3. Set the time interval for the sine wave (`t`).
4. Plot the sine waves dynamically for each frequency.

## Code Overview
### Key Parameters
- `f1` and `f2`: Starting and ending frequencies.
- `fp`: Number of frequency points to generate.
- `t`: Time interval for sine wave generation.

### Example Code Snippet
```matlab
f1 = 10000; % Starting frequency (10 kHz)
f2 = 10000000; % Ending frequency (10 MHz)
fp = 100; % Number of frequency points
t = linspace(0, 0.000001, 5000); % Time vector
f = linspace(f1, f2, fp); % Linear frequency scaling

for i = 1:fp
    figure(1)
    y = 4 * sin(2 * pi * f(i) * t); % Sine wave generation
    plot(t, y, 'r', 'Linewidth', 3);
    pause(1);
end
```

## Usage Instructions
### Prerequisites
- MATLAB (any recent version should work)

### Steps to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/shawrajdeep00/Variable-frequency-Sine-wave-generator.git
   ```
2. Open the `Variable-frequency-Sine-wave-generator` folder in MATLAB.
3. Edit the parameters in the code (`f1`, `f2`, `fp`, etc.) to suit your requirements.
4. Run the script in the MATLAB environment.
5. Observe the dynamic sine wave plots.

### Example Visualization
- Sine waves with increasing frequencies will be displayed in real time.
- Adjust the `pause` parameter to control the speed of plotting.

## Applications
- Signal processing demonstrations
- Waveform analysis and research
- Educational purposes for understanding frequency variation
- Testing and debugging frequency-dependent systems

## Customization
Feel free to modify the following parameters:
- **Frequency Range**: Adjust `f1` and `f2` to change the start and end points.
- **Number of Frequency Points**: Change `fp` to increase or decrease the resolution.
- **Time Interval**: Modify `t` to suit your waveform duration.

## Contributing
Contributions are welcome! If you have suggestions for improvement or additional features, feel free to submit a pull request or open an issue.

## Feedback
If you find this project useful or have any questions, please don't hesitate to reach out through the GitHub repository's [Issues](https://github.com/shawrajdeep00/Variable-frequency-Sine-wave-generator/issues) section.
