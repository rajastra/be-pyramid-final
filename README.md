# Tugas uas pwl

## how to run

1. clone this repo

```bash
git clone
```

2. change directory to this repo

```bash
cd final-project-pwl
```

3.  change development.ini url to your database url

```bash
sqlalchemy.url = mysql+pymysql://username:password@localhost:5432/dbname
```

4. install dependencies

```bash
 pip install -e .
```

5. migrate database

```bash
alembic -c development.ini upgrade head
```

6. load database

```bash
initialize_pwl_final_db development.ini
```

5. run

```bash
pserve development.ini --reload
```

6. run test

```bash
pytest
```

## Documentation

```
https://documenter.getpostman.com/view/23098382/2s9YknANiZ
```

## api routes Auth Service

| Route                        | Method | Description |
| ---------------------------- | ------ | ----------- |
| {{URL}}/api/v1/auth/login    | POST   | login       |
| {{URL}}/api/v1/auth/register | POST   | register    |

## api routes Product Service

| Route                                 | Method | Description                |
| ------------------------------------- | ------ | -------------------------- |
| {{URL}}/api/v1/product                | POST   | Create Product             |
| {{URL}}/api/v1/product/{{PRODUCT_ID}} | POST   | Update Product             |
| {{URL}}/api/v1/product/{{PRODUCT_ID}} | GET    | Get Product by Id          |
| {{URL}}/api/v1/product/{{PRODUCT_ID}} | DELETE | Delete Product             |
| {{URL}}/api/v1/product?search=        | GET    | Get Product All and Search |

## api routes Service Cart

| Route                   | Method | Description                 |
| ----------------------- | ------ | --------------------------- |
| {{URL}}/api/v1/cart     | POST   | Add data product to Cart    |
| {{URL}}/api/v1/cart?id= | GET    | Get data Cart by User Id    |
| {{URL}}/api/v1/cart?id= | DELETE | Delete data Cart by User Id |

## api routes Service Order

| Route                | Method | Description           |
| -------------------- | ------ | --------------------- |
| {{URL}}/api/v1/order | POST   | Checkout Product User |
| {{URL}}/api/v1/order | GET    | Get Data Order User   |
