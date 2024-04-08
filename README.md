# ESWA_dataset

This is a dataset repository for accessing all evaluation data for automatic summarization using Llama 2 models that have been fine-tuned.

# Dataset Overview

This dataset is a compilation of fact-checking reports from two distinct sources: Politifact for English reports and Demagog for Czech reports. Each dataset shares the same column structure but caters to different languages.

## Dataset Structure

- `id`: The unique identifier corresponding to each fact-checking report.
- `source_text`: The complete fact-checking report provided by the sources.
- `target_text`: The original summary as provided by the fact-checking site.
- `source_text_shorter`: An extractive summary of the fact-checking report, generated using the Local Outlier Factor algorithm. For Baseline models, this column is empty since the extractive summary is not utilized; the `source_text` is directly fed to the transformer model instead.
- `text`: The interpretation of the input text, formatted to suit the requirements of the Llama 2 model.
- `generation_text`: The final output from the transformer, which has undergone generation and post-processing.

## Additional Details

- The dataset includes both entire reports (`source_text`) and summaries (`target_text`), allowing for a comparison between detailed reports and their summarized counterparts.
- The `source_text_shorter` serves as a feature for advanced models that utilize summaries for processing, providing a condensed version of the report for quicker understanding and analysis.
- The `text` column is particularly formatted for the Llama 2 model, indicating that the dataset can be used to train or validate the performance of this model.
- The `generation_text` represents the end product of the transformer's processing and is the content that would be used for dissemination or further analysis.

## Usage

This dataset can be valuable for evaluating LLM models on the task of fact-checking summarization. It is particularly useful for understanding the effectiveness of extractive summaries and the transformation of such summaries into coherent, final outputs.


