# Organizing Medical Transcriptions

This project uses OpenAI's GPT models to extract structured information from medical transcription data, including patient age, recommended treatment/procedure, and corresponding ICD codes. The workflow is implemented in a Jupyter Notebook using Python and pandas.

## Features
- Loads medical transcription data from a CSV file.
- Uses OpenAI API to extract patient age and recommended treatment/procedure from each transcription.
- Retrieves ICD codes for the recommended treatment/procedure using OpenAI.
- Outputs a structured DataFrame with the extracted information.

## Requirements
- Python 3.8+
- pandas
- openai
- json
- Jupyter Notebook

## Setup
1. Clone or download this repository.
2. Install dependencies:
   ```sh
   pip install pandas openai jupyter
   ```
3. Place your `transcriptions.csv` file in the project directory. The CSV should have at least the following columns:
   - `transcription`: The medical transcription text.
   - `medical_specialty`: The medical specialty for each transcription.
4. Set your OpenAI API key as an environment variable:
   ```sh
   set OPENAI_API_KEY=your-api-key-here
   ```
   (On Linux/macOS, use `export` instead of `set`.)

## Usage
1. Open `main.ipynb` in Jupyter Notebook.
2. Run all cells to process the transcriptions and generate the structured output.

## Output
- The notebook will create a DataFrame (`df_structured`) containing:
  - Age
  - Recommended Treatment/Procedure
  - Medical Specialty
  - ICD Code

## Notes
- The OpenAI API is used for both information extraction and ICD code lookup. Ensure your API key has sufficient quota.
- If a field cannot be extracted, it will be marked as 'Unknown'.

## License
This project is for educational and research purposes only. Not for clinical use.
