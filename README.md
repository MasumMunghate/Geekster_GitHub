# Geekster_Pokemon

fetchPokemonDetails Function:
This function is responsible for fetching data for the first 150 Pokémon using the PokeAPI.
It creates an array of promises (promises) for each Pokémon request.
It uses fetch to request Pokémon data and converts the responses to JSON.
The promises are collected in the promises array, and Promise.all is used to wait for all promises to resolve.
Once all data is fetched, it maps through the data to create a simplified Pokémon object and stores it in the pokemonDetails array.
Finally, it calls createPokemonCard for each Pokémon object to create and display Pokémon cards.

createPokemonCard Function:
This function takes a Pokémon object as an argument and creates an HTML card element to display the Pokémon's information.
It creates elements for the Pokémon's ID, image, name, abilities, and type.
The function sets appropriate content and adds these elements to the card.
The card is then added to the cardsContainer element.

Search Functionality:
When the user clicks the "Search" button (searchButton), an event listener triggers this function.
It retrieves the value entered in the search bar (searchBar) and converts it to lowercase for case-insensitive matching.
It filters the pokemonDetails array based on the search input.
It clears the cardsContainer and creates Pokémon cards only for the filtered results

Reset Functionality:
When the user clicks the "Reset" button (resetButton), an event listener triggers this function.
It clears the cardsContainer to remove any displayed Pokémon cards.
It then calls fetchPokemonDetails to reload and display the first 150 Pokémon.

Initial Fetching:
The fetchPokemonDetails function is called initially to fetch and display information about the first 150 Pokémon when the page loads.

this code provides a basic Pokémon search and display functionality using data fetched from the PokeAPI. Users can search for Pokémon by name, and the corresponding Pokémon cards are displayed. They can also reset the display to show all Pokémon again.
