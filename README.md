# Probability Calculator

## Introduction

This project involves creating a program to estimate the probability of drawing certain balls randomly from a hat. The task is to implement a Hat class and an experiment function in Python.

## Hat Class

Create a Hat class in `prob_calculator.py` with the following specifications:

- The class should take a variable number of arguments that specify the number of balls of each color in the hat.
- For example:
  ```python
  hat1 = Hat(yellow=3, blue=2, green=6)
  hat2 = Hat(red=5, orange=4)
  hat3 = Hat(red=5, orange=4, black=1, blue=0, pink=2, striped=9)
hat is `{"red": 2, "blue": 1}`, `contents` should be `["red", "red", "blue"]`.

- The `Hat` class should have a `draw` method that accepts an argument indicating the number of balls to draw from the hat.
- This method should remove balls at random from `contents` and return those balls as a list of strings.
- The balls should not go back into the hat during the draw, similar to an urn experiment without replacement.
- If the number of balls to draw exceeds the available quantity, return all the balls.

## Experiment Function

Create an `experiment` function in `prob_calculator.py` (not inside the Hat class) with the following specifications:

- This function should accept the following arguments:
  - `hat`: A hat object containing balls that should be copied inside the function.
  - `expected_balls`: An object indicating the exact group of balls to attempt to draw from the hat for the experiment.
  - For example, to determine the probability of drawing 2 blue balls and 1 red ball from the hat, set `expected_balls` to `{"blue":2, "red":1}`.
  - `num_balls_drawn`: The number of balls to draw out of the hat in each experiment.
  - `num_experiments`: The number of experiments to perform. (The more experiments performed, the more accurate the approximate probability will be.)

- The `experiment` function should return a probability.

## Usage

For example, if you want to determine the probability of getting at least two red balls and one green ball when you draw five balls from a hat containing six black, four red, and three green. To do this, you will perform N experiments, count how many times M you get at least two red balls and one green ball, and estimate the probability as M/N.

Here is how you would call the `experiment` function based on the example above with 2000 experiments:

```python
hat = Hat(black=6, red=4, green=3)
probability = experiment(hat=hat,
                  expected_balls={"red":2,"green":1},
                  num_balls_drawn=5,
                  num_experiments=2000)
