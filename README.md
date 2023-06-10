# Education app

To roll migrations, if there is no alembic.ini file yet, you need to run the following command in the terminal:

```
alembic init migrations
```

After that, a folder with migrations and a configuration file for alembic will be created.

- In alembic.ini, you need to set the address of the database into which we will roll the migrations.
- Then we go to the folder with migrations and open env.py, there we make changes to the block where it is written

```
from myapp import mymodel
```

- Next, enter: ```alembic revision --autogenerate -m "comment"```
- Migration will be created
- Next, enter: ```alembic upgrade heads```
