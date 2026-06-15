### Assessment Task 2
____________________________________________________________________________________________________________________________________________________________________________________________________________________
## PART A: Data Selection and Attributes.

6 Attributes:
| Listed In Order From Most To Least Powerful |:
1. Top Speed:
This attribute describes the maximum speed that the specific model of car can acheive in standard road conditions. This attribute is useful for both users and manufacturers as it gives insight to the driver of how much tire speed is required, ensures you can cruise at highway speeds without straining the engine whilst additionally giving insight into how robust and reliable the vehicle is. This attribute was chosen as it stands as a universal marker of car superiority, performance and respect. However this could overshadow other attributes too much giving top speed too much of an advantage, this signifies power limits of specific attributes need to be applied carefully and effectively.
2. Car Intelligence /99
This attribute describes the non essential technological aspects that a car possesses and measures them on a scale of how advanced they are. For example modern teslas with automated driving, smart assistance, voice command controls and remote controllig would score higher than traditional toyota corolla's that have limited intelligence compared to newer models. This attribute also heavily serves as an indicator of car safety as features such auto lane correction, crash avoidance, speeding avoidance, parking assistance and a birdseyeview hazard detection system increases user awareness, safety and can be applied to significantly reduce the amount of crashes and traffic penalties an overall cohort or individual experiences. This attribute as chosen due to its growing revelance and technological uprising, its being deployed as a way to reduce crahses and increase user enjoyment and comfort. As this measure yields great power it needs to be balanced and proportionalised to prevent abuse in game. 
3. Acceleration
This Attribute accurately measures how quickly/powerfully a car reaches a specific speed. This is commonly tested by using a nort to 60 measurement to determine how fast a car gets fast or in a more scientific way the rate at which an object (car) changes its velocity. This measurement is extremely useful as it gives users insight into the safety of their vehicle in situations such as traffic lights stops, heavy traffic or around animals. Electric Vehicles generally have superior acceleration due to the engine not requiring as much start up power to reach its top speed. This attribute also serves as baseline marker of car performance and superiority meaning its an essential measurement to determine what card is superior. This should be proprotioanlised easily and will not contribute to abuse.
4. Strain Gauge
This Attribute is utilised to determine the material robusticity and strength that the car possesses. It serves as a baseline marker of design integrity and material choice indicating a cars strength and performance. It is often measured using pressure tests at specific car failure and strength points. These results are then quantified using machines that measure material plasticity and malleability. These measurements serve as both useful to the user and manufacturer as they demonstarte how much a vehicle can handle in terms of physical load, crash durability and specififc weather conditions. This attribute was carefully hand picked as it serves as an overall marker of durability making it specifically important for modern road and weather conditions. This marker is not a major attribute but is a significant stat meaning it needs to be proportionalised in the rating system.
5. Car Type Ev/Hybrid/Petrol
This attribute depicts the cars fuel source and environmental sustainability by distinguishing it to be one of the 3 major categories. Whether a car is traditional petrol, Ev ir a hybrid will determine its environemtal friendliness, acceleration potential as well as its maximum range. This attribute is heavily relevant today with climate concerns and the evergrowing transition into EV/Hybrid Cars. The hybrid model will deliver the most points then followed by the ev then petrol for this category.
6. Price
This attribute will serve as a value marker and instead of attributing points due to more affordability it will attribute more points the higher the price is.
____________________________________________________________________________________________________________________________________________________________________________________________________________________
## PART B: Class Design.

Overview:

# Car:()

Attributes:

> * private int carID
> * private String make
> * private String model
> * private int year
> * private int topSpeed
> * private int carIntelligence
> * private double acceleration
> * private int strainGauge
> * private String carType
> * private double price
> * private String imagePath
> * private int overallRating

Methods:

> * public void calculateOverallRating()
> * public int getAttribute(String attributeName)
> * public void displayCarInfo()
> * public void updateCarDetails()
> * public Card convertToCard()

Description:() This class serves as the base unit of competition allowing the system to draw and create cards.

# Card:()

Attributes:()

> * private int cardID
> * private Car car
> * private Player owner
> * private boolean isInPlay
> * private int cardValue

Methods:()

> * public void displayCard()
> * public int compareAttribute(String attributeName, Card opponentCard)
> * public void assignOwner(Player player)
> * public int getCardValue()
> * public void setInPlay(boolean status)

Description:() This class serves as the playable versions of the cars.

# Deck:()

Attributes:()

> * private ArrayList<Card> cards
> * private int deckSize
> * private ArrayList<Card> discardPile
> * private int currentCardIndex

Methods:()

> * public void createDeck()
> * public void shuffleDeck()
> * public void dealCards(int numberOfPlayers)
> * public Card drawCard()
> * public void addCard(Card card)
> * public void removeCard(Card card)
> * public boolean isEmpty()
> * public void resetDeck()

Description:() This serves as the place the cards are stored and can be maniuplated by the player.

# Player:()

Attributes:()

> * private int playerID
> * private String playerName
> * private ArrayList<Card> hand
> * private int score
> * private int roundsWon
> * private boolean isCurrentTurn
> * private Card activeCard

Methods:()

> * public void drawCard(Deck deck)
> * public Card playCard()
> * public String chooseAttribute()
> * public void receiveCard(Card card)
> * public void addPoint()
> * public void incrementRoundsWon()
> * public Card getTopCard()
> * public boolean hasCardsRemaining()
> * public void displayHand()

Description:() This is the player and here is where actions that the player can take to play will be executed.

# Game:()

Attributes:()

> * private int gameID
> * private ArrayList<Player> players
> * private Deck deck
> * private int currentRound
> * private Player currentPlayer
> * private Player winningPlayer
> * private String gameStatus
> * private Player roundWinner
> * private ArrayList<Card> cardsInBattle

Methods:()

> * public void startGame()
> * public void setupPlayers()
> * public void dealCards()
> * public void playRound()
> * public void compareCards()
> * public Player determineRoundWinner()
> * public void awardCardsToWinner()
> * public void switchTurn()
> * public boolean checkGameOver()
> * public Player determineGameWinner()
> * public void displayLeaderboard()
> * public void restartGame()
> * public void endGame()

Description:() This allows the system to interact with turns from players and terminate, start and manipulate the game.
____________________________________________________________________________________________________________________________________________________________________________________________________________________
