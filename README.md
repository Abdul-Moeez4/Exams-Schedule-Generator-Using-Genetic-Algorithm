# Exam Schedule Generator Using Genetic Algorithm

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [How It Works](#how-it-works)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Input Files](#input-files)
- [Output](#output)
- [Genetic Algorithm Components](#genetic-algorithm-components)
- [Constraints](#constraints)
- [Sample Output](#sample-output)
- [Evaluation](#evaluation)
- [Report](#report)
- [License](#license)

## Overview
This project implements a Genetic Algorithm (GA) to automatically generate optimal exam schedules for universities. It ensures all hard constraints are met (like no overlapping exams) while optimizing for preferences (like breaks between exams).

## Features
- Custom implementation of Genetic Algorithm without using GA libraries
- Handles complex scheduling constraints:
  - No student exam overlaps
  - Teacher availability
  - Classroom assignments
  - Time slot management (weekdays 9AM-5PM)
- Optimizes for preferences:
  - Friday lunch breaks
  - Minimizing back-to-back exams
  - Preferred ordering of MG/CS courses
- Visual output with color-coded schedules

## How It Works
1. **Initialization**: Creates initial population of random schedules
2. **Fitness Evaluation**: Scores each schedule based on:
   - Hard constraints (must pass)
   - Soft constraints (optimization)
3. **Selection**: Uses roulette wheel selection to choose parents
4. **Crossover**: Combines parent schedules (single-point crossover)
5. **Mutation**: Randomly modifies schedules (5% mutation rate)
6. **Termination**: Stops after 100 generations or valid solution

## Requirements
- Python 3.8+
- Required packages:
  ```bash
  pandas
  numpy
