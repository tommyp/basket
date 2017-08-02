## Description of the problem


A new restaurant has joined Deliveroo and only sells three products:

```
+--------------|----------------|---------+
| Product Code |     Name       |  Price  |
+--------------|----------------|---------+
|     MC1      |   Mac & Cheese |  £3.11  |
|     BR1      |   Burger       |  £5.00  |
|     PZ1      |   Pizza        | £11.23  |
+--------------|----------------|---------+
```

Our CEO is a big fan of buy-one-get-one-free offers and of Mac & Cheese. He wants us to add a rule to do this.

The COO, though, likes low prices and wants people buying Burgers to get a price
discount for bulk purchases. If you buy 3 or more Burgers, the price should drop to £4.50.
Our restaurant basket can add items in any order, and because the CEO and COO change
their minds often, it needs to be flexible regarding our pricing rules.

The interface to our checkout looks like this (shown in Ruby):

```
ba = Basket.new(pricing_rules)
ba.add(item)
ba.add(item)
price = ba.total
```

Implement a checkout system that fulfills these requirements in Ruby.

Here is some test data:

```
Basket items: MC1, BR1, MC1, PZ1
Total price expected: £19.34
```

```
Basket items: MC1, MC1
Total price expected: £3.11
```

```
Basket items: BR1, BR1, MC1, BR1
Total price expected: £16.61
```
