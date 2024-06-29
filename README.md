# Steam App Requirements / Approach 

## Original Idea / Objective:
Create an app that can track a user’s steam inventory and its value similar to the way Robinhood tracks stocks. This will effectively treat a user’s inventory like a skin portfolio. 

## Requirements for this Part1: (prioritize ui function over form)
- Frontend UI to see skins and prices
- Make a way to import inventory 
- Backend API for getting skins (steam user inventory link) 
- Backends API for getting prices (need to determine frequency of getting prices)
- Make a refresh button for inventory. 


## Requirements for this Part2:
- Make ui look good
- MongoDB Atlas to store skin data / price data 
- Make CRUD operations for items in UI inventory
- Create a way to sync settings in the UI (ability to keep tracking items that left your inventory)
- Create a wishlist ( need to reflect accurate prices. Updated regularly)
## Requirements for this Part3:
- Make a user system
- Track change over time
- User should be tied in with steam inventory iD
- UI shows Steam Market as well as skinport/other markets.(definite maybe)

## Stack:
- ReactJS Frontend. (eventually run in AWS or something? Look into this)
- Terraform Backend with AWS Lambda APIs
- Maybe MongoDB if it makes sense. If Mongo, then use Atlas
- Snyk for security scanning

## Approach:
### Part1:
- Look into a steam API that will work for your usecase
- Setup terraform for lambdas
- Build backend api calls to steam api first
  - Fetch skin data based on steam user inventory url
  - Fetch prices for skins if the steamAPI doesn’t already do that
- Image data ideal if possible
- Structure (Lamba) API JSON response:
  - Skin name
  - Quantity of skin
  - Price
  - priceTime
  - totalValue
- UI textbox for steam inventory url
- Have React component with 4 inputs 
  - Name
  - Quantity 
  - Price
  - Image if possible
- Display all response data using this react component
- Hydrate components
- Display total value

Todo: make landing page mockup. 
### Part2: tbd (this is agile BABY)


Lead Develope: Andrew Cruz
Lead Consultant: Joe Wang
