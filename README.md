# Cash Flow Minimizer

**Project Overview:**

The objective of this project is to streamline multiple financial transactions into fewer exchanges, simplifying the process and making it more efficient. The project utilizes a heap-based data structure, which can be depicted as a directed graph, to achieve this goal.

**Algorithm Breakdown:**

To implement the algorithm, take the following steps for each individual, indexed from 0 to n-1:

1. **Calculate Net Amounts**: For each person, compute the net amount owed or due. This is done by subtracting the total debts from the total credits for that individual.
  
2. **Identify Extreme Cases**: Determine which individual has the highest credit (creditor) and which has the highest debt (debtor). Let's call the maximum creditor `Pc` with a credit of `maxCredit` and the maximum debtor `Pd` with a debt of `maxDebit`.
  
3. **Reconcile Balances**: Identify the smaller of the two amounts, `maxCredit` or `maxDebit`. This smaller value, `x`, is transferred from `Pd` to `Pc`. This reduces the debt for `Pd` and the credit for `Pc`.
  
4. **Update Sets**: 
   - If `x` equals `maxCredit`, remove `Pc` from the list of individuals and repeat the process for the remaining people (n-1).
   - If `x` equals `maxDebit`, remove `Pd` from the list of individuals and continue with the same recursive approach for the remaining (n-1).

The process continues until all transactions are reconciled, resulting in a reduced number of total transactions.

**Screenshots:**

![Screenshot (155)](https://github.com/anilrai4001/cash-flow-minimizer/assets/79553966/b0fcb094-9b36-4ac4-a67f-7d33d629af2d)
![Screenshot (156)](https://github.com/anilrai4001/cash-flow-minimizer/assets/79553966/a3e7dd4f-c9b3-4be3-a453-b1f9b95114b0)
