# SAW Decision Support System

A web-based decision support system using the Simple Additive Weighting (SAW) method to help evaluate and rank alternatives based on multiple criteria. This project allows users to input criteria (columns) with respective weights and types (Benefit or Cost), enter data for each alternative (rows), and then calculate rankings based on the weighted scores.

## Features

- **Add Criteria**: Input the name, weight (between 0 and 1), and type (Benefit or Cost) for each criterion.
- **Add Data**: Input data for each alternative (row) based on the defined criteria.
- **SAW Calculation**: Automatically calculate the weighted scores for each alternative using the SAW method.
- **Ranking**: Display the final rankings based on the calculated scores.

## How It Works

1. **Define Criteria**:
   - Add criteria such as "Price", "Quality", "Availability", etc., each with a weight (between 0 and 1) and type (Benefit or Cost).
2. **Input Data**:

   - For each criterion, input values for various alternatives. For example, "Price" might be a cost type, while "Quality" could be a benefit type.

3. **Calculate Rankings**:

   - After entering data, the system normalizes the values, applies the weights, and calculates a final score for each alternative.
   - Alternatives are ranked based on their final scores, with the best alternative having the highest score.

4. **Result Display**:
   - The matrix of input values, normalized values, weighted values, and final rankings are displayed to the user.

## Technologies Used

- **HTML**: For structuring the page.
- **CSS**: For styling (via Bootstrap).
- **JavaScript (jQuery)**: For dynamic interactions and calculations.
- **SAW (Simple Additive Weighting)**: A multi-criteria decision analysis method used for ranking and decision-making.

## Installation

To run this project locally, follow these steps:

1. Clone this repository:

   ```bash
   git clone https://github.com/Korewah/SAW-DecisionSupportSystem.git
   ```

### Penjelasan:

- **Note**: Bagian baru ini ditambahkan di akhir README untuk menginformasikan kepada pembaca bahwa penggunaan bahasa Indonesia dalam penamaan variabel dilakukan dengan tujuan kemudahan bagi pengembang lokal dan bahwa perubahan ke bahasa Inggris akan dilakukan di pembaruan berikutnya.
