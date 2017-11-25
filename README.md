# ecommerce-website-with-complete-backend
Note: You must be connected to VPN to view this website securely.

This backend web porject sattisfies all these requirements:


Requirements:
This site will consist of at least 5 PHP files: index.php, cart.php, admin.php, DB.class.php and lib_project1.php (you may choose to have additional pages)
Each page will share common graphic elements, and will have a global navigation system that links to every other page. These common elements MUST be achieved through the use of functions or a template system. Points will be deducted if common code (HTML or PHP) is copied on more than one page.
These pages will be located in the student's /home/abc1234/Sites/756/project1/ folder on Kelvin.
The site should have an aesthetically pleasing design. 
When planning your code and design, you need to make sure the site can be “re-arranged” without changing the content-generating script coding. You can achieve this in one of two ways: 
Through the extensive use of <div id/class> tags and changing the order of creating the sections of the pages and CSS files OR
Through the use of a template system, where you read in the template file replacing placeholders with content (a different template would provide a different look for the same content) in conjunction with CSS files.
CSS (in external style sheets) should be used extensively.
The site will pass HTML5 validation.
ALL DATABASE QUERIES MUST BE PARAMETERIZED QUERIES USING PREPARED STATEMENTS.

index.php
Will include:

A "sales" section, which will have any products that have discounted prices highlighted in this section. For each discounted product, it will include an image, a brief description, the original price, sale (discounted) price and quantity left.
You will have a minimum of 3 discounted items at one time and at most 5 discounted items at one time.
A "catalog" section that will list all of the products available. For each product, it will include an image, brief description, price and quantity left. This information will display 5 items at a time with a paging scheme to view the next/previous page of items. If an item is discounted, do not include it in this section of the page. The pagination must be done on the server, not on the client.
Each item, whether in the sales or catalog section, will have a "buy/add to cart" button that when clicked will add that item to a "cart" (a table in your MySQL database) and will decrease the quantity on hand (including updating the products table and the web page).
You will have a minimum of 15 products for sale.
The products are loaded dynamically from a MySQL database (products table). The format for each item should be:
Product Name | Description | Price | Quantity | Image Name | Sale Price
The sale price will be 0 if the item is NOT on sale (i.e., not discounted).

cart.php
Will include:

A listing of all items in the cart with a total amount the purchase included. 
You should only include the product name, the description, quantity ordered, and cost for the item. Do not include the image.
There should be a button that will clear (empty) the cart (i.e remove items and display an “Empty Cart” message). Emptying the cart will update the quantity on hand for all items that were in the cart.
The information here will come from a "cart" table in the db.
DB.class.php
Will contain all of your database access logic

It will use parameterized queries

lib_project1.php
Will include most of your application code

The code in this file will be structured as reusable functions that will be called by the other pages.
Copious comments will describe the inputs, outputs, and purpose of each function.
You should create functions that go beyond what we did in class.
This file will be included (or required) by the other pages.
Can you structure this file as a class, or multiple classes, with the appropriate corresponding file names, if you prefer.

admin.php
Will:

Pick an item to edit and save the changes. Make sure that the number of discounted items constraint doesn’t get violated.
Add an item for purchase. The picture can be on the server already (or, for above and beyond, allow uploading of a picture). Again, if it has a discounted price, make sure to follow the constraint.
No editing or adding will be done without authentication. Authenticate the user against a table in the database and create a session for the user.
