# Market-Basket Analysis on Amazon Book Reviews

This project applies **market-basket analysis** techniques to the [Amazon Books Review dataset](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews) to uncover relationships between books reviewed by the same users. The goal is to identify frequent itemsets and generate association rules that highlight meaningful reading patterns.

## Overview
- Dataset: Amazon Books Review (Kaggle)
- Algorithm: Apriori (via `mlxtend`)
- Key Metrics: Support, Confidence, Lift

## Key Findings
- Several strong associations were found between popular titles such as *The Hobbit* and *The Lord of the Rings*.
- High lift values (>100) indicate strong co-occurrence among related or series books.
