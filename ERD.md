category
-
category_id PK VARCHAR
category VARCHAR 

subcategory
-
subcategory_id PK VARCHAR
subcategory VARCHAR

contacts
-
contact_id PK INT
first_name VARCHAR
last_name VARCHAR
email VARCHAR

campaign
-
cf_id PK INT
contact_id INT FK >- contacts.contact_id
company_name VARCHAR
description VARCHAR
goal FLOAT
pledged FLOAT
outcome VARCHAR
backers_count INT
country VARCHAR
currency VARCHAR
launch_date DATE
end_date DATE 
category_id VARCHAR FK >- category.category_id
subcategory_id VARCHAR FK >- subcategory.subcategory_id
