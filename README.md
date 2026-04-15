# Concept-Visualization-in-Manim
Linear Regression Visualized On Basketball

# Linear Regression Animation

This Jupyter notebook contains a Manim animation that visually explains the concepts of linear regression using NBA player data (minutes per game vs. points per game).

## Description

The animation walks through the key steps of linear regression:

1. **Data Visualization**: Scatter plot of the data points
2. **Best-Fit Line**: Derivation of the OLS (Ordinary Least Squares) equation
3. **Residuals**: What the line misses and sum of squared residuals
4. **R²**: Proportion of variance explained
5. **Prediction**: Using the model to predict new values

## Prerequisites

- Python 3.7+
- Jupyter Notebook
- Manim (Community edition recommended)
- NumPy

## Installation

1. Install Manim:
   ```bash
   pip install manim
   ```

2. Install other dependencies:
   ```bash
   pip install numpy jupyter
   ```

3. For headless rendering (recommended for servers):
   ```bash
   pip install manim[gui]  # or just manim if you have a display
   ```

## Usage

### Running Individual Scenes

Each scene can be rendered individually using the `%%manim` magic command in Jupyter cells:

```python
%%manim -ql SceneName
```

Available scenes:
- `TitleScene`: Opening title card
- `DataCloudScene`: Data visualization
- `FittedLineScene`: OLS derivation and line fitting
- `ResidualsScene`: Residual analysis
- `PredictionScene`: Model prediction example
- `SummaryScene`: Recap of concepts

### Rendering the Full Animation

To render the complete animation:

```python
%%manim -ql BasketballRegression
```

This combines all scenes into one video.

### Command Line Rendering

You can also render scenes from the command line:

```bash
manim -ql linear_animation.py SceneName
```

Note: You'll need to extract the Python code from the notebook cells to a .py file for command-line rendering.

## Output

The animation generates MP4 video files in the `media/videos/` directory. Quality options:
- `-ql`: Low quality (fast rendering)
- `-qm`: Medium quality
- `-qh`: High quality (slow rendering)

## Data

The animation uses simulated NBA player data with realistic noise. The true relationship is approximately 0.55 points per minute played.

## Customization

You can modify:
- Colors and styling in the color palette section
- Data points in the `MINUTES` and `POINTS` arrays
- Animation timings and effects in each scene
