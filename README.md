## DjangoShop
### An E-commerce application made using Django.

## Overview
<p>
DjangoShop is a Django based E-commerce application where users can browse for products, add them to their cart, go through the checkout process and pay with a credit card to order the products.
</p>

## Installation
Make sure you have **Python**,**Celery** and **RabbitMQ** installed in your system.

Clone the repository

    https://github.com/abhinav2499/DjangoShop.git


Install all required dependencies in an isolated environment

    cd DjangoShop
    pipenv install django
    pipenv shell
    pipenv install -r requirements.txt
    
For payment integration, go to following link to create a **Braintree sandbox account** and find your Merchant ID, Public Key and Private Key:
    
    https://www.braintreepayments.com/sandbox

Edit **settings.py** and add your Merchant ID, Public Key and Private Key in it:
    
    BRAINTREE_MERCHANT_ID = 'Your Merchant ID'
    BRAINTREE_PUBLIC_KEY = 'Your Public Key'
    BRAINTREE_PRIVATE_KEY = 'Your Private key'
    
 ## Running on local server
 By default, the database for development server in **DjangoShop/db.sqlite3** is already filled with some data for ease of development.
 
 If you want to start clean then **delete db.sqlite3** and follow this step:
 
 ### Create migrations
 
    python manage.py makemigrations
    python manage.py migrate
    
### Create superuser

    python manage.py createsuperuser
    
### Run the server

    python manage.py runserver
