CSE 476 – Final Project Report:

This repository contains the implementation for my CSE 476 Final Project.
The project builds an agent that generates final answers for the course test-set using the model API provided and outputs them in JSON.

How to Run the Project:

Install dependencies (Python 3.8+ recommended):
pip install requests

Place the test data file in the same directory:
cse_476_final_project_test_data.json

Run the answer generation script:
python generate_answer_template.py

The script will update:
cse_476_final_project_answers.json

This file contains the final answers which is required.

Project Description:

The project uses a simple agent pattern:
Reads each question from the test dataset, 
Sends a request to the API, 
Enforces “final answer only” with no reasoning, 
Writes all outputs to a JSON array with the required schema, 
Validates output file structure before finishing, 
The script hardcodes the required API settings:

api_key = "cse476"
base_url = "http://10.4.58.53:41701/v1"
model_name = "bens_model"

Reproducibility:

To reproduce the results:
Ensure API access to the course server.
Place the test dataset file next to the script.

Run:
python generate_answer_template.py

The script will automatically do the following:
Query every question,
Produce final answers,
Validate that the JSON is acceptable.
