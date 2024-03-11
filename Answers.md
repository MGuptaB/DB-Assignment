1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
   
Ans:- 
  The relationship between the "Product" and "Product_Category" entities can be described as follows:
  In the "Product" entity:
  Each product belongs to one specific category.
  The "category_id" column in the "Product" table serves as a foreign key that references the primary key "id" in the "Product_Category" table.
  This relationship indicates that each product is associated with one and only one category.

  In the "Product_Category" entity:
  Each category may have multiple products associated with it.
  The "id" column in the "Product_Category" table serves as the primary key, uniquely identifying each category.
  Products are categorized based on shared characteristics or attributes, and the "Product_Category" table stores the information about these categories.

  Therefore, the relationship between "Product" and "Product_Category" is a one-to-many relationship, where each product belongs to one category, but each category can have multiple associated products.

2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
   
Ans:-
  To ensure that each product in the "Product" table has a valid category assigned to it, you can enforce referential integrity using foreign key constraints. Here's how you could achieve this:

  Define Foreign Key Constraint: In the database schema definition, when creating or altering the "Product" table, you specify a foreign key constraint on the "category_id" column. 
  This constraint ensures that any value entered into the "category_id" column must already exist in the primary key column of the "Product_Category" table. For Example:-

   ALTER TABLE Product
   ADD CONSTRAINT fk_product_category
   FOREIGN KEY (category_id)
   REFERENCES Product_Category(id);

   By implementing foreign key constraints, you can ensure data integrity and maintain consistency between the "Product" and "Product_Category" tables.
