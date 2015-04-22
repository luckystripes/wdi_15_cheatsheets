#PostgreSQL

```Database Management System (DBMS)```

	* SQLite, is just like a big CSV text file. Postgres, on the other hand, consists of a database and a daemon server.
	
	* Your rails app is running on its own server and interacts with the Postgres daemon server
	
	* To access Postgres in your terminal, enter psql
	
	* In Postgres in terminal, type \h to see what's available
	
	* To quit, type \q
	
	* Rails works exactly the same with Postgres as it does with SQLite, so you should use Postgres from the get-go ideally. 
	


###To create a new Rails app with Postgres instead of SQLite:
	1. rails new <appname> -d postgresql
	2. rails g scaffold <model> <attributes:types>
	3. rake db:create
	4. rake db:migrate
	5. rails s

###To change a Rails app from SQLite to Postgres:
	1. Open the gemfile of the application
	2. Replace the 'sqlite3' gem to 'pg'
	3. Go to the database.yml file in the config directory
		b. Under default, make sure to have:
			i. Adapter: postgresql
			ii. Encoding: unicode
			iii. Pool: 5
		c. Under development, make sure to have:
			i. <<: *default
			ii. database: <projectname>_development
    4. In terminal, do a rake db:create, followed by a rake db:migrate