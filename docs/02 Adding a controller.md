# Adding a controller

This is a 3 step process

1. Go to app/controllers and create a new file <<**name**>>_controller.rb, where the content of the file will be as follows
```
class <<Name>>Controller < ApplicationController
    def <<page_name>>
    end
end
```
where 
- <<**name**>> and <<**Name**>> will be the controller name, note the capital letter in the class name, it is important
- <<page_name>> is the name of the page we'll link the definition to

2. Go to app/views and create a <<**name**>> folder to store the html file that will be rendered when we call such controller/route, within the recently created folder we'll add a new file <<page_name>>.html.erb, note we're still using the names we choose before for the controller and its definition

3. Open config/routes.rb and add the new page/route for the app to show the new page
```
Rails.application.routes.draw do
...
  <<protocol>> '<<name>>/<<page_name>>'
...
end
```
where <<**protocol**>> will be either post,get,put,delete depending on the action we want for the route

If we want that the new route will be the main page loaded when we load the root of the app we simply replace the <<**protocol**>> for root:
```
Rails.application.routes.draw do
...
  root '<<name>>/<<page_name>>'
...
end
```