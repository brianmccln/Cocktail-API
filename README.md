# JavaScript Project
## thecocktaildb.com API
The **Cocktail-API.html** page uses **fetch()** 
### here are 3 ways to get cocktails: 
- **search input**: input keyword /ingredient
- **select menu**: choose keyword / ingredient
- **random button**: click to get random cocktail
- **letter buttons**: click to get random cocktail
ALL 3 ways call the same function: **getCocktail**

**API endpoints used**
- Search box and select menu request cocktails by **name** from **endpoint**:  
**www.thecocktaildb.com/api/json/v1/1/search.php?s=margarita**  
- Random button requests a random cocktail from **endpoint**:  
**www.thecocktaildb.com/api/json/v1/1/random.php**  
- Letter button requests all cocktails starting with that letter from **endpoint**:  
**www.thecocktaildb.com/api/json/v1/1/search.php?f=a**  

**API returns an object w ONE key: "drinks"**
the drinks array values are all objects, one per drink
each obj has lots of keys; the ones we want are:  
- **strDrink** (name of drink)  
- **strInstructions** (how-to-make text)  
- **strDrinkThumb** (url of drink image on API server)  
- **strIngredient1** - **strIngredient15**  
  (each property is one ingredient string instead of having all ingredients in an array); 
- if less than 15 ingredients, those values are all null  
- **strMeasure1** - **strMeasure15** works same as ingredient props  