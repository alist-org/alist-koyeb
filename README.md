# alist-koyeb

The fastest way to deploy the alist to koyeb is to click the **Deploy to Koyeb** button below.

[![deploy to koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?type=docker&image=xhofe/alist:latest&ports=5244;http;/&name=alist&env[PORT]=5244&env[DB_TYPE]=mysql&env[DB_HOST]=host&env[DB_PORT]=3306&env[DB_USER]=alist&env[DB_PASS]=password&env[DB_NAME]=alist&env[DB_TABLE_PREFIX]=alist_&env[DB_SSL_MODE]=false&env[CDN]=https://cdn.jsdelivr.net/npm/alist-web@$version/dist)

Update the environment variables as follows:

`DB_TYPE:` mysql (you can also use sqlite3 and postgres. mysql is for remote db)

`DB_HOST:` provide db host address here (keep blank for sqlite3 db)

`DB_USER:` provide db username here (keep blank for sqlite3 db)

`DB_PASS:` provide db password here (keep blank for sqlite3 db)

`DB_TABLE_PREFIX:` alist_ (keep as it is)

`CDN:` https://cdn.jsdelivr.net/npm/alist-web@3.28.0/dist (you can also use other CDN. but this CDN is tested and working.)

`DB_PORT:` 3306 (keep as it is)

`PORT:` 5244 (keep as it is)

`DB_NAME:` provide db name here (keep blank for sqlite3 db)

`DB_SSL_MODE:` false (only if you use mysql or postgres db. for sqlite3 this env variable is not needed)

N.B: During deploying keep watching the deploy logs to get the admin password. It will be appeared as initial password: <password> text. For remote db you can't change it later using `./alist admin` command.

### database
You may need to use another remote MySQL database as instance restarts will lose data.
Recommended Free MySQL Databases:
- https://db4free.net/
- https://remotemysql.com/
- https://www.freesqldatabase.com/

### password
The initial password is randomly generated, and you can get it by checking the `Runtime logs`.
