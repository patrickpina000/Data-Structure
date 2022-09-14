# Data-Structure
The ABC Hardware Company has hired you to program its Accounts Receivable department. (A/R are accounts that owe money to the company for purchases from the company)

There are two types of input data

A master file in ascending order by customer number, containing a 4-digit customer number, a 20-character customer name and a balance due.

A transaction file containing records of each transaction by each customer. This file is in ascending order by customer number. There should be more than one transaction record per master record. Each related group of data in a file is called a record. A record should be stored in a structure.


Each record starts with a character, O for order or P for payment. Each also contains the four-digit customer number, a four-digit transaction number, plus up to three more values:

If the code is “O”, the record contains the item ordered (20 characters), the quantity ordered (an integer) plus the cost of the item. (You must multiply to get the total cost). In addition some of these may have an additional field with a number like 20 (or any other number between 5 and 30) which would mean after computing the cost due to a promotion they are getting that discount from the company for these items. So, if a company ordered $800 worth of merchandise and it is followed by a 30 in the file they will get a discount of $240 off the order and the order will only cost them $560. Remember only some of the records should have a discount. 

If the code is “P”, the record contains the amount of the payment and a possible 2nd field which is a % discount for early payment off their total balance based on the amount they are currently paying. For example, if the payment is $500 and it has a 20 in the second field, they should get an additional 20% off the balance so a payment of $500 will give them an additional $100 off their balance. These should be only on some, not all, of the payment records.  

You are to read in records one at a time from the two files and use the transaction file records to update the master file. Process all transaction records for each master record before going on to the next master record. If the transaction record contains an “O” in column 1 calculate the order amount and add it to the balance due. If the record contains a “P” in Column 1 subtract the payment from the balance due. Keep a running total of the A/R Balance of ABC Company (that is the sum of the balances due for each customer). 

Your program should 

Check for errors such as duplicate master records or records in the transaction file with a customer number that does not appear in the master file.

After processing a master record and all its transaction records prepare an invoice for each customer which lists on top the customer name and number, a line depicting the previous balance (the original balance in the master record before any transactions) followed by the transactions and the a balance due. 

It should look like this

Customer Name    	Customer Number

					Previous Balance     $xxxxxxxxxx.xx

transaction number			item ordered		order amount
transaction number			item ordered		order amount
transaction number 		payment		payment amount
transaction number			item ordered		order amount

					Balance Due		$xxxxxxxxx.xx


Don’t forget payments reduce balances orders increase balances. You are to create your own data using at least 7 to 10 customers with an average of 4 to 5 transactions each.

