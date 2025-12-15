# Market-Basket Analysis on Amazon Book Reviews

This project implements a scalable market-basket analysis on the Amazon Books Reviews dataset. Each user is treated as a transaction (basket) containing the set of books they reviewed. The goal is to identify frequent books and frequent book pairs that commonly appear together across users.
The project focuses on frequent itemset mining (L1 and L2) using a manual implementation of the Apriori algorithm, enhanced with global frequency pruning and random sampling to handle the large size of the dataset efficiently.

# Dataset
Source: Amazon Books Reviews Dataset (Kaggle)
Size: ~3 million original reviews

Final processed data:
-- 66,082 user baskets
-- 472 retained book items after pruning
Each basket represents all books reviewed by a single user.

## Key Findings
- Several strong associations were found between popular titles such as *The Hobbit* and *The Lord of the Rings*.
- High lift values (>100) indicate strong co-occurrence among related or series books.
