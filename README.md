# figure-out-dinner-app
A web app that takes a list of ingredients and tells you various recipes


So imagine an app with a user model that takes in all your ingredients, and within missing one or ingredients, give you a list of recipes.


### Phase 1:

 USER can enter a list of ingredients
 
 USER can select various filters for the generated recipes 
 
 USER can provide which recipes they used
 
 USER can order delivery of food items they are missing in a selected recipe using InstaCart like service (optional)
 
 
 ### Phase 2: (If possible?)
 
 USER can use phone's camera to detect ingredients in their fridge
 
 
 This will be a flask backend api server with a Typescript/React frontend.
 Will host on AWS CloudFront and ECS
 
 ## Discovery
 
 1. Recipe api? (AllRecipe)
    - [Edamam](https://developer.edamam.com/edamam-docs-recipe-api)
    - [BigOven](https://api2.bigoven.com/web/documentation/recipes)
 2. ingredient recognition model/dataset?
 3. Model out how to show recipes will one or two things missing (food delivery feature)
 4. Support and Performance issues with Camera API / Tensorflow.js 
 
 ### Data
 
1. User model CRUD
    - email
    - phone ?
2. Recipe Preferences 
    - Diet
    - CuisineType
    - Diet restrictions
3. Search recipes by current ingredients
4. Liked Recipes


### Endpoints
 
####`/register`
####`/signin`
 
#### GET/POST `/user-preferences`
Get your current preferences as a user or save the entire preferences state to the user
 
#### GET `/search`
Call recipe api with a search query of list of ingredients with preferences from the user model

#### POST `/user/{user_id}/like-recipe/{recipe_id}`
Have a user like a recipe 