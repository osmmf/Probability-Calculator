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
