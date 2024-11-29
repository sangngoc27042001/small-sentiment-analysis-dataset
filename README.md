# Customer Feedback Analysis Dataset

This repository contains a dataset of customer feedback and its corresponding sentiment analysis for a bakery business. The dataset consists of two main JSON files that are paired by index, meaning each entry in the input file corresponds to the same-indexed entry in the evaluation file.

## Dataset Structure

### 1. Input Customer Comments (`input_custommer_comment.json`)

Contains customer feedback in three formats:

- `org_comment`: Original customer comment (primarily in Vietnamese)
- `reconstructed_comment`: Cleaned and reconstructed version of the original comment
- `eng_comment`: English translation of the comment

Example:
```json
{
    "org_comment": "bánh ngon á, đc mí c chỗ t khen nè",
    "reconstructed_comment": "Bánh ngon á, được mấy chị chỗ tôi khen nè.",
    "eng_comment": "The cake is delicious, my colleagues praised it."
}
```

### 2. Ground Truth Evaluation (`evaluation/groud_truth.json`)

Contains detailed analysis of each comment with:

- `sentiment`: Categorization of the sentiment (positive/negative/neutral)
- `original_text`: The specific text being analyzed
- `problem`: Any identified issues or problems (null if none)
- `company_function_involed`: The relevant business function (e.g., Product, Customer Service, etc.)

Example:
```json
{
    "points": [
        {
            "sentiment": "positive",
            "original_text": "The cake is delicious",
            "problem": null,
            "company_function_involed": "Product"
        }
    ]
}
```

## Business Functions Covered

The dataset captures feedback across various business functions including:

- Product: Quality, taste, and presentation of bakery items
- Offline Customer Services: In-store service experience
- Online Customer Services: Digital ordering and communication
- Digital Marketing: Online presence and promotions
- Packaging: Delivery and product packaging

## Dataset Usage

This dataset can be used for:

1. Sentiment Analysis: Understanding customer satisfaction levels
2. Problem Identification: Detecting common issues and areas for improvement
3. Business Function Analysis: Evaluating performance across different aspects of the business
4. Customer Experience Mapping: Understanding the customer journey and pain points

The paired nature of the dataset (input and evaluation) makes it valuable for training and validating sentiment analysis models, especially for Vietnamese language processing in the food service industry context.
