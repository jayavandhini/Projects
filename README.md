# Image Puzzle Solver & Recipe Recommendation App

This project combines two applications:
1. **Image Puzzle Solver** - Breaks an image into a grid, shuffles it, and reassembles it using a hill-climbing algorithm.
2. **Recipe Recommendation System** - Fetches and recommends recipes based on user-provided ingredients and dietary restrictions using the Spoonacular API.

---

## Table of Contents
1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [How It Works](#how-it-works)
4. [Setup Instructions](#setup-instructions)
5. [Usage](#usage)
6. [API Key Setup](#api-key-setup)
7. [Sample Outputs](#sample-outputs)
8. [Future Enhancements](#future-enhancements)
9. [License](#license)

---

## Features

### Image Puzzle Solver
- Splits an image into a 3x3 grid.
- Uses a **hill-climbing algorithm** to minimize pixel mismatch and rearrange the pieces.
- Visualizes the shuffled and solved puzzles.

### Recipe Recommendation System
- Fetches recipes using the **Spoonacular API**.
- Scores and recommends recipes based on user-provided ingredients.
- Considers dietary restrictions such as vegan, gluten-free, etc.

---

## Tech Stack
- **Programming Language**: Python
- **Libraries Used**:
  - `PIL (Pillow)` - For image processing.
  - `NumPy` - For numerical operations and pixel mismatch calculations.
  - `Matplotlib` - To visualize the puzzles.
  - `Requests` - To fetch recipes from the Spoonacular API.
  - `Random` & `Copy` - For implementing the hill-climbing algorithm.

---

## How It Works

### Image Puzzle Solver
1. The input image is split into a grid of 3x3 pieces.
2. A **hill-climbing algorithm** iteratively swaps pieces to minimize the total pixel mismatch at their borders.
3. The final optimized configuration is visualized and reassembled into an image.

### Recipe Recommendation System
1. Users provide a list of ingredients and dietary restrictions.
2. The program fetches recipes from the **Spoonacular API**.
3. Recipes are scored based on ingredient matches and dietary preferences.
4. The top recipes are displayed as recommendations.

---

## Setup Instructions

### Prerequisites
- Python 3.x installed on your system.
- Install the required libraries using pip:

```bash
pip install pillow numpy matplotlib requests
```

### Project Files
Ensure the following files are in the project folder:
- **`main.py`** - The main script combining both functionalities.
- **Input Images** - Image files like `samosa.jpg`, `test4.jpg`, etc.

---

## Usage

### 1. Image Puzzle Solver
Run the script to visualize puzzles for different images:

```bash
python main.py
```

The script processes four sample images: `samosa.jpg`, `test4.jpg`, `test3.jpg`, and `test.jpg`. It splits, shuffles, and attempts to reassemble them.

### 2. Recipe Recommendation System
To fetch and recommend recipes:
- Update the `user_ingredients` list and `dietary_restrictions` in the script.

Example:
```python
user_ingredients = ['chicken', 'rice', 'broccoli']
dietary_restrictions = ['gluten-free']
```
Run the program to fetch and display the top recipes:
```bash
python main.py
```

---

## API Key Setup
The recipe system uses the Spoonacular API. Obtain an API key:
1. Visit [Spoonacular API](https://spoonacular.com/food-api).
2. Create an account and get your API key.
3. Replace the placeholder in the script:

```python
API_KEY = 'YOUR_API_KEY_HERE'
```

---

## Sample Outputs

### Image Puzzle Solver
- **Before Optimization**: The puzzle is randomly shuffled.
- **After Optimization**: Pieces are rearranged to minimize border mismatches.

### Recipe Recommendation
```
Recommended Recipes:
1. Chicken and Rice Bowl
2. Gluten-Free Broccoli Stir Fry
3. Lemon Garlic Chicken
```

---

## Future Enhancements
- Implement advanced algorithms like Genetic Algorithms for faster convergence.
- Allow dynamic grid sizes (e.g., 4x4, 5x5).
- Add more dietary options (e.g., keto, paleo).
- Add a user interface for better accessibility.

---

