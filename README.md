# Audience Segmentation
By Elliot Kim

I used various NLP techniques to label data that looks like `- OnAudience > Intent > Electronics > Video > Televisions` with a label like `Technology`. Prior to this, I used regex (e.g., if data contains 'Electronic', label as 'Technology') and managed to label 74% before labeling further became too inefficient with diminishing returns. Using transformers, I successfully labeled 95% of the data points, reducing the coverage deficit by 5.3x.

## Quick Links
- The cleaned dataset: [data_cleaned.csv](https://github.com/elliot-d-kim/audience-segmentation/blob/main/data_cleaned.csv)
- The code to create it: [audience_segmentation_abridged.ipynb](https://github.com/elliot-d-kim/audience-segmentation/blob/main/audience_segmentation_abridged.ipynb)

## Overview of code

### Preprocess data

- Format data: Fix encoding format
- Clean up data
    - Remove insignificant null values
    - Clean up misformatted delimiters
- Tokenize + Remove noisy tokens

### Label data using NLP

- Provide categories with sample of associated words
- Enhance importance of words at tail end of 'Audience Segmentation' (i.e., the details)
- Create embeddings of data
- Train transformer and label data
- Review by hand

### Clean up
- Remove unnecessary data from final dataset
- Save as [data_cleaned.csv](https://github.com/elliot-d-kim/audience-segmentation/blob/main/data_cleaned.csv)
 
