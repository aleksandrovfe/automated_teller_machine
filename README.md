# Automated teller machine (ATM)

## Glossary 
- user - person who uses service
- cardId - unique id of the user card(contains numbers and letters(lower/upper case)) contains 16 characters
- card number - unique number contains 10 characters
- card pin - digits that user created to get acess to card in the ATM, contains 4 characters
- client - atm machine
- server - a computer with installed software 
- request - is data package transferred from the client to the server
- respone - is data package transferred from the server to the client
- -> - redirect to page

## Elements 
- enter card number and card pin page
- header: shows exit button
- cardId defining service to authorize the user and get user info
- menu page: uses user info to define ui, shows buttons (withdraw money, check how much money is in stock)
- withdraw money page: enter how much money withdraw, withdraw button
- check how much money is in stock: shows how much money user has
- error message component: shows message with error text in the left bottom corner


## Concerns 

- ATM shows enter card number and card pin page as a default page
- user can enter card number and card pin to get access to the card 
  - if card number - valid and card pin refer to this card -> menu page 
  - else - show an error(wrong credentials) 
- in menu page user can chooses option (-> withdraw money, -> check how much money is in stock
- in withdraw money page,  display return to the menu button -> menu page, user can input amount of how much he wants to withdrow and after clicking on withdrow btn check how much money yser has
  - if money < user's input, than shows an error(money is no enought), 
  - else current user stock minus user input, than withdrow money to user -> main page
- in check how much money is in stock page user can see hom much money he has, display return to the menu button -> menu page
- header component has exit button which clear user info from the client and -> enter card number and card pin page

