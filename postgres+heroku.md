#PostgreSQL & Heroku
---

### Description :
###### This Cheatsheet details how to create a rails app using postgresql as well as switching over to postgresql from sqlite.
---
###### This Cheatsheet also shows how to deploy to heroku once your app is ready for production
---
#### Setting up PostgresSQL & Heroku (All steps involved)
---
1.  ##### Creating a new rails app using postgresql

```
rails new <app_name> -d postresql -T
```

2. ##### Switching over to PostgreSQL from SQLite
   ###### In the Gemfile
   ```
   gem 'pg'
    ```

   ###### In config/database.yml
   ```
  default: &default
  adapter: postgresql
  encoding: unicode
  pool: 5
  timeout: 5000
  development:
  <<: *default
  database: app_name_development
  ```

3. ##### Also in the Gemfile
	```
	ruby "2.2.1"  #This goes at the start of the file

	```

	```
	gem 'rails_12factor', group: :production
	```

	(This gem enables serving 	assets in production and 		setting your logger to standard 	out, both of 	which are required 	to run a Rails 4 application on 	a twelve-factor provider, such 	as Heroku.)



4. 	##### In the terminal (Make sure you're in the correct directory)
	```
	bundle install

	rake db:create

	rake db:migrate
	```


5. ##### If you haven't already create an account and sign in to Heroku

	```
	https://www.heroku.com/
	```
##### Download the tool belt
	```
	https://toolbelt.heroku.com/
	```

6. ##### In the terminal

	```
	heroku login
	Email: (enter your email)
	Password (enter your password - it will show blank and that's fine)

	heroku create #creates a new URL for your app
	cd <app_name>

	git add .
	git commit -m "Initial Commit"
	git push heroku master

	heroku open #opens the app on heroku

	heroku rename <app_name> #Replace "app_name" with your own name.

	```



---

###Made by Rushindra Sinha & Kyle Conkright
