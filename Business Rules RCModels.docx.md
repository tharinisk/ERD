# **Business Rules — RC Models Company**

## **Customer Entity**
- Customer must have a unique customer ID
- Customer must have a unique email address
- Customer must have first name and last name
- Customer must have a shipping address
- Customer must have a phone number
- Customer can optionally have a subscription status
- Customer can optionally have preferred payment methods
- Customer can have multiple shipping addresses

## **Salesperson Entity**
- Each salesperson must have a unique employee ID
- Each salesperson must have first name and last name
- Each salesperson must have contact information
- Each salesperson must have hire date

## **Salesperson-Invoice**
23. A salesperson can create many invoices
24. Each invoice must be created by exactly one salesperson

## **Invoice Entity**
- Each invoice must have a unique invoice number
- Each invoice must have a date
- Each invoice must have a total amount
- Each invoice must have a status (paid, pending, cancelled)
- Each invoice must have shipping information

## **Invoice-Payment**
25. Each invoice must have exactly one payment
26. A payment belongs to exactly one invoice

## **Payment Entity**
- Each payment must have a unique payment ID
- Each payment must have amount
- Each payment must have payment date
- Each payment must have payment method (credit card, PayPal, Apple Pay)
- Each payment must have payment status

## **Product Category Entity**
- Each category must have a unique category ID
- Each category must have a name
- Each category must have a description

## **Product-Category**
27. Each product must belong to exactly one category
28. A category can have many products

## **Inventory Entity**
- Each inventory record must have a unique ID
- Each inventory record must have quantity in stock
- Each inventory record must have last updated timestamp
- Each inventory record must have reorder level

## **Product-Inventory**
29. Each product must have exactly one inventory record
30. Each inventory record belongs to exactly one product

## **Subscription Entity**
- Each subscription must have a unique subscription ID
- Each subscription must have start date
- Each subscription must have status (active/inactive)
- Each subscription must have subscription type

## **Customer-Subscription**
31. A customer can have one subscription
32. A subscription belongs to exactly one customer

## **Return/Refund Entity**
- Each return must have a unique return ID
- Each return must have return date
- Each return must have reason
- Each return must have status
- Each return must have refund amount

## **Invoice-Return**
33. An invoice can have multiple returns
34. Each return must be associated with exactly one invoice

## **Additional Constraints**

35. Every invoice must have at least one line item
36. Customer email address must be unique
37. Vendors and manufacturers are separate
38. Promotions are independent of purchases
39. Inventory quantity cannot be negative
40. Payment amount must match invoice total
41. Return date must be after invoice date
42. Subscription can only be active for one customer at a time
43. Salesperson ID must be valid employee ID
44. Return amount cannot exceed original invoice amount