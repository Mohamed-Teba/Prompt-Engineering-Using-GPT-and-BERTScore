# Prompt Engineering using GPT-2 & BERTScore:

This repository contains a Jupyter Notebook implementation of a prompt engineering using the GPT-2 model to generate motivational text. The generated outputs are evaluated against a human-written reference using BERTScore, and results are presented in a table.

## Table of Contents

- Project Overview
- Installation
- Usage
- Project Structure
- Prompts
- Human-Written Reference
- Evaluation
- Contributing
- License

## Project Overview

The purpose of this project is to demonstrate prompt engineering techniques by:

- Designing five distinct prompts to generate motivational content using GPT-2.
- Generating three outputs per prompt (15 total).
- Evaluating the outputs against a human-written motivational quote using BERTScore.
- Presenting the evaluation results in a table.

The project is implemented in a Jupyter Notebook (`prompt_engineering_assignment.ipynb`), which includes all code, prompts, outputs, and results.

## Installation

### Prerequisites

- Python 3.6 or higher
- Jupyter Notebook or JupyterLab
- Git (to clone the repository)
- A compatible environment (local machine or cloud platforms like Google Colab)

### Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/prompt-engineering-assignment.git
   cd prompt-engineering-assignment
   ```

   Replace `your-username` with your GitHub username.

2. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

   The `requirements.txt` includes:

   - `transformers`
   - `bert_score`
   - `torch`
   - `pandas`

3. Verify that Jupyter Notebook is installed:

   ```bash
   pip install jupyter
   ```

## Usage

1. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```
2. In the Jupyter interface, navigate to the repository directory and open `prompt_engineering.ipynb`.
3. Run all cells in the notebook by selecting **Run &gt; Run All Cells** or pressing **Shift + Enter** for each cell.
4. The notebook will:
   - Install dependencies (if not pre-installed).
   - Load the GPT-2 model with a random seed for reproducibility.
   - Define and display five distinct prompts.
   - Generate three motivational outputs per prompt (15 total).
   - Provide a human-written reference quote with a source link.
   - Evaluate outputs using BERTScore.
   - Display results in a table with Prompt Type, Output #, and BERTScore F1 columns.
5. Review the printed outputs, reference, and evaluation results in the notebook.

Alternatively, you can upload `prompt_engineering_assignment.ipynb` to Google Colab and run it there, as the notebook includes a cell to install dependencies.

## Project Structure

```plaintext
prompt-engineering/
├── prompt_engineering.ipynb  # Main Jupyter Notebook with implementation
├── requirements.txt                     # Python dependencies
└── README.md                           # Project documentation (this file)
```

- `prompt_engineering.ipynb`: Contains the complete implementation, including setup, prompt design, text generation, reference, evaluation, and results.
- `requirements.txt`: Lists required Python packages for easy installation.
- `README.md`: Provides an overview, setup instructions, and usage details.

## Prompts

The project uses five distinct prompts to generate motivational content:

1. **Direct**: "Write a motivational quote about overcoming challenges."
2. **Scenario-based**: "Imagine you're encouraging a student who is struggling with self-doubt before an exam. Write a motivational message."
3. **Persona-based**: "As a seasoned life coach, write a quote about finding purpose in life."
4. **Keyword-based**: "Using the words 'resilience', 'dreams', and 'courage', write an inspiring message."
5. **Conversational**: "User: I'm feeling unmotivated and stuck. GPT-2: Here's an inspiring quote for you:"

Each prompt generates three outputs, resulting in 15 total texts.

## Human-Written Reference

The generated outputs are compared to the following human-written motivational quote:

> "The greatest glory in living lies not in never falling, but in rising every time we fall."

**Source**: BrainyQuote - Nelson Mandela

## Evaluation

The outputs are evaluated using BERTScore, which measures semantic similarity between each generated text and the human reference. The results are presented in a table with:

- **Prompt Type**: The prompt category (e.g., Direct, Scenario-based).
- **Output #**: The output number (1, 2, or 3).
- **BERTScore F1**: The F1 score, rounded to four decimal places.

The table is generated using `pandas` and displayed in markdown format for clarity.

## Contributing

This project is an assignment submission and not actively seeking contributions. However, feedback, suggestions, or bug reports are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request with a clear description of your changes.

Please ensure your contributions align with the project's educational purpose.

## License

This project is licensed under the MIT License. The human-written reference quote is sourced from BrainyQuote with proper attribution. All code and documentation are free to use, modify, and distribute under the terms of the MIT License.

---

**Notes**:

- The notebook sets a random seed (`set_seed(42)`) for reproducible GPT-2 outputs.
- GPT-2 is configured with `max_length=60`, `temperature=0.7`, and `top_p=0.9` for controlled generation.
- BERTScore uses the English language model (`lang="en"`) for evaluation.
- For performance, ensure sufficient memory (local or cloud) when running GPT-2 and BERTScore.