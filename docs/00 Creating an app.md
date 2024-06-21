# Creating a Ruby on Rails app

After installing and configuring ruby and rails in the equipment we need to change directory to the folder we want the app to reside

Once there we simply use 

```
rails new <<name_of_the_app>> -T -d <<database>>
```
where 
* name_of_the_app: Name we want our app to have and the name of the folder it will be created
* database: Database manager to be used; mysql, sqlite, postgresql, oracle, etc

the former command will create a folder with the given name and initialize the config file to use the database we selected, if no DB namager is selected sqlite will be the default, then later we'll have to change that when we move the app to prod
