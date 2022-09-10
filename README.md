# alist-koyeb

The fastest way to deploy the alist to koyeb is to click the **Deploy to Koyeb** button below.

[![deploy to koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?type=docker&image=xhofe/alist:v2.6.4&ports=8080;http;/&name=alist&env[DB_TYPE]=sqlite3&env[DB_HOST]=host&[DB_PORT]=3306&env[DB_USER]=alist&env[DB_PASS]password=&[DB_NAME]=alist&env[DB_TABLE_PREFIX]=alist_&env[CACHE_EXPIRATION]=60&env[CLEANUP_INTERVAL]=120&env[ASSETS]=https://npm.elemecdn.com/alist-web@$version/dist)

### database
You may need to use another remote MySQL database as instance restarts will lose data.
Recommended Free MySQL Databases:
- https://db4free.net/
- https://remotemysql.com/
- https://www.freesqldatabase.com/

### password
The initial password is randomly generated, and you can get it by checking the `Runtime logs`.
