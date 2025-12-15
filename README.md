# Market-Basket Analysis on Amazon Book Reviews

This project implements a scalable **market-basket analysis** on the Amazon Books
Reviews dataset. Each user is treated as a transaction (basket) containing the set
of books they reviewed. The goal is to identify **frequent books** and **frequent
book pairs** that commonly appear together across users.

The project focuses on **frequent itemset mining (L1 and L2)** using a manual
implementation of the **Apriori algorithm**, enhanced with **global frequency
pruning** and **random sampling** to efficiently handle a large dataset.

---

## Dataset

- **Source:** Amazon Books Reviews Dataset (Kaggle)  
- **Original size:** ~3 million reviews  

**Final processed data:**
- 66,082 user baskets  
- 472 retained book items after pruning  

Each basket represents all books reviewed by a single user.

## Key Findings

- **Frequent single items (L1):** 357 books  
- **Frequent book pairs (L2):** 1302 pairs (using MIN_SUPPORT = 0.008)

- Lower support thresholds produce more frequent itemsets, but introduce weaker
  and less interpretable patterns. Higher thresholds reduce noise but discard
  useful associations. A support value of **0.008** provides a good balance.

- The sampling approach preserved almost all frequent itemsets while
  significantly reducing computational cost:
  - 362 candidate items → 357 confirmed  
  - 1304 candidate pairs → 1302 confirmed  

- Many frequent pairs correspond to **different editions or related books from
  the same series**, reflecting realistic co-reading behavior.

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

## Reference

Mohamed Bakhet. *Amazon Books Reviews Dataset*. Kaggle.  
https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews

