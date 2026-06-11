🛒 Instacart Customer Reorder Behavior — Scenario Analysis Project
This project analyzes customer reorder behavior using the Instacart Online Grocery dataset and a custom machine‑learning model that predicts reorder probability under multiple behavioral scenarios. The final deliverable is an interactive Tableau dashboard that allows users to explore how different customer behavior patterns affect reorder rates across departments and hours of the day.

The dashboard includes:

A scenario selector (Baseline, Weekend Peak, Loyalty, Budget‑Conscious)

A KPI showing overall predicted reorder rate

A department‑level breakdown of reorder probability

A time‑of‑day analysis of reorder probability

Fully dynamic visuals that update based on the selected scenario

📊 Summary of Findings
1. Overall Reorder Rate
Across all scenarios, the model predicts an average reorder probability of ~72%, indicating strong customer loyalty and repeat purchasing behavior.

2. Department-Level Insights
Some departments show consistently high reorder rates (e.g., produce, dairy/eggs, pantry), while others show lower reorder likelihood (e.g., household, babies, alcohol).
Scenario changes affect departments differently — for example:

Weekend Peak increases reorder probability in convenience‑oriented departments.

Loyalty Scenario boosts reorder rates in staple categories like dairy, produce, and pantry.

Budget-Conscious Scenario reduces reorder probability in premium or specialty departments.

3. Hour-of-Day Behavior
Reorder probability peaks during late morning to early afternoon, with a noticeable dip in late evening hours.
Weekend Peak scenarios amplify midday activity, reflecting real‑world shopping patterns.

🧠 Project Workflow
1. Data Preparation
Loaded Instacart datasets (orders, products, aisles, departments).

Engineered features such as:

Order hour of day

Day of week

Department and aisle identifiers

Prior order behavior

2. Model Training
Trained a neural network classifier to predict reorder probability.

Generated scenario‑based predictions by modifying behavioral inputs.

3. Scenario Generation
Created four scenario datasets:

Baseline

Weekend Peak

Loyalty

Budget‑Conscious

Each scenario modifies customer behavior assumptions and produces new predicted reorder probabilities.

4. Tableau Dashboard
Connected scenario prediction CSV files

Built dynamic visuals

Added a parameter‑driven scenario selector

Applied a scenario filter to all worksheets

🛠 Dependencies
Python Dependencies
If you want to reproduce the model or generate new scenario predictions:

Python 3.9+

pandas

numpy

scikit‑learn

tensorflow / keras

matplotlib / seaborn

jupyter notebook (optional)

Install with:

bash
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn
Tableau Dependencies
Tableau Desktop or Tableau Public

CSV files exported from the model:

scenario_predictions_for_tableau.csv

scenario_predictions_for_tableau (1).csv

scenario_predictions_for_tableau (2).csv

A working parameter named Scenario Selector

A calculated field named Scenario Filter

▶️ How to Run the Project
1. Generate Scenario Predictions (Python)
Run the notebook or script that:

Loads Instacart data

Trains the model

Outputs scenario prediction CSVs

2. Load Data into Tableau
Open Tableau

Connect using Text File (NOT Excel)

Load the scenario prediction CSV

Create the Scenario Selector parameter

Create the Scenario Filter calculated field

Build the dashboard using the provided worksheets

3. Interact With the Dashboard
Use the Scenario Selector to switch between scenarios and observe changes in:

Overall reorder rate

Department reorder behavior

Hour‑of‑day reorder probability

📁 Repository Structure
Code
/data
    aisles.csv
    departments.csv
    products.csv
    orders.csv
    scenario_predictions_for_tableau.csv
    ...

/notebooks
    model_training.ipynb
    scenario_generation.ipynb

/dashboard
    instacart_scenario_dashboard.twbx

README.md
📌 Author
Joshua Zimmerman‑Gibson  
ECPI University — B.S. Computer Information Science
Concentration in AI, Machine Learning, and Data Analytics
