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
## PART C: Class Design.

Overview:

┌───────────────────────────────────────┐
│                 Car                   │
├───────────────────────────────────────┤
│ - carID : int                         │
│ - make : String                       │
│ - model : String                      │
│ - year : int                          │
│ - topSpeed : int                      │
│ - carIntelligence : int               │
│ - acceleration : double               │
│ - strainGauge : int                   │
│ - carType : String                    │
│ - price : double                      │
│ - imagePath : String                  │
│ - overallRating : int                 │
├───────────────────────────────────────┤
│ + calculateOverallRating() : void     │
│ + getAttribute(String) : int          │
│ + displayCarInfo() : void             │
│ + updateCarDetails() : void           │
│ + convertToCard() : Card              │
└───────────────────────────────────────┘
                  │
                  │ Association
                  ▼
┌───────────────────────────────────────┐
│                 Card                  │
├───────────────────────────────────────┤
│ - cardID : int                        │
│ - car : Car                           │
│ - owner : Player                      │
│ - isInPlay : boolean                  │
│ - cardValue : int                     │
├───────────────────────────────────────┤
│ + displayCard() : void                │
│ + compareAttribute(                   │
│   String, Card) : int                 │
│ + assignOwner(Player) : void          │
│ + getCardValue() : int                │
│ + setInPlay(boolean) : void           │
└───────────────────────────────────────┘
          ▲                     ▲
          │                     │
          │ owns                │ owner
          │                     │
          │                     │
┌───────────────────────┐   ┌───────────────────────────┐
│        Deck           │   │          Player           │
├───────────────────────┤   ├───────────────────────────┤
│ - cards : ArrayList   │   │ - playerID : int          │
│ - deckSize : int      │   │ - playerName : String     │
│ - discardPile         │   │ - hand : ArrayList<Card>  │
│ - currentCardIndex    │   │ - score : int             │
├───────────────────────┤   │ - roundsWon : int         │
│ + createDeck()        │   │ - isCurrentTurn : boolean │
│ + shuffleDeck()       │   │ - activeCard : Card       │
│ + dealCards(int)      │   ├───────────────────────────┤
│ + drawCard() : Card   │   │ + drawCard(Deck) : void   │
│ + addCard(Card)       │   │ + playCard() : Card       │
│ + removeCard(Card)    │   │ + chooseAttribute()       │
│ + isEmpty() : boolean │   │   : String                │
│ + resetDeck()         │   │ + receiveCard(Card)       │
└───────────────────────┘   │ + addPoint()              │
          ▲                 │ + incrementRoundsWon()    │
          │                 │ + getTopCard() : Card     │
          │                 │ + hasCardsRemaining()     │
          │                 │   : boolean               │
          │                 │ + displayHand() : void    │
          │                 └───────────────────────────┘
          │
          │ Composition
          │
          ▼
┌────────────────────────────────────────────┐
│                   Game                     │
├────────────────────────────────────────────┤
│ - gameID : int                             │
│ - players : ArrayList<Player>              │
│ - deck : Deck                              │
│ - currentRound : int                       │
│ - currentPlayer : Player                   │
│ - winningPlayer : Player                   │
│ - gameStatus : String                      │
│ - roundWinner : Player                     │
│ - cardsInBattle : ArrayList<Card>          │
├────────────────────────────────────────────┤
│ + startGame() : void                       │
│ + setupPlayers() : void                    │
│ + dealCards() : void                       │
│ + playRound() : void                       │
│ + compareCards() : void                    │
│ + determineRoundWinner() : Player          │
│ + awardCardsToWinner() : void              │
│ + switchTurn() : void                      │
│ + checkGameOver() : boolean                │
│ + determineGameWinner() : Player           │
│ + displayLeaderboard() : void              │
│ + restartGame() : void                     │
│ + endGame() : void                         │
└────────────────────────────────────────────┘

Game ◆────────── Deck
Game ◆────────── Player (2..*)

Deck ◆────────── Card (0..*)

Player ◆──────── Card (0..*)

Card ──────────► Car
Card ──────────► Player

Player ─ ─ ─ ─► Deck   (dependency: drawCard())
Car ─ ─ ─ ─ ─► Card    (dependency: convertToCard())
____________________________________________________________________________________________________________________________________________________________________________________________________________________
## PART D: Game Mechanics
This Car themed car game is heavily based around the original Top Trumps card game, players will compete by comparing 6 specific attributes of their cards unique to this game. Each card represnts a unique car and will store all of the attribute values.

1. Top Speed

2. Car Intelligence

3. Acceleration

4. Strain Gauge

5. Car Type

6. Price

The end objective of this game is to win rounds by strategically handpicking select attributes from your current deck and defetaing your opponent in a comparison.

## How a round is played
1. At the start of a round the whole deck should be shuffled and all cards should be distributed in an even fashion amongst all players.
2. Each player collates their cards in a stack.
3. A player is selected to reveal their top card.
4. That player selects an attribute on their card to compete with.
5. All other players select their top card and the attribute is comapred to see who hass the winning hand.
6. All cards utilized during the round are placed into the winners collection.
7. The winner becomes the current player and repeats the process.

## How Attributes are Selected
The player who won the previous round selects the attribute for the next comparison.

The six available attributes are:

1. Top Speed – Higher value wins.

2. Car Intelligence (/99) – Higher value wins.

3. Acceleration – Lower 0–60 time wins because the car accelerates faster.

4. Strain Gauge – Higher value wins.

5. Car Type – Compared using a points system:

Hybrid = 3 points

EV = 2 points

Petrol = 1 point

6. Price – Higher value wins.

The selected attribute is applied to all cards currently in play for that round.

## How Winners are Determined
Afte rplayers reveal their cards the winning attribute is delegated the winner of that round.

They then:
1. Receive all the cards dealt in that round.
2. Gain a point on the leaderboard.
3. Becomes the selecting player of the next round.

If 2 or more players have an attribute of the same value and are tied in first position for that round the player will select another card and battle the same attribute initially selected, this can happen as many times as neccessary and the winner will collect all cards and gain a point normally.

## How the Game Ends
The game ends when one or more of these conditions are met:

1. A player collects every single card in the allocated deck.
2. A player violently kills, incapacitates or scares the other players causing them to be unable to play.
3. A violent event such as a school shooting, fire or natural disaster immeditaley threatens the players.
4. Another commitment disrupts the game.

Once/If a winner has been determined:

* The final leaderboard is displayed.

* Statistics such as score, rounds won and cards collected are shown.

* Players may choose to restart the game using the restartGame() method or end the session using endGame().
____________________________________________________________________________________________________________________________________________________________________________________________________________________
## PART E: Interface and Card Design
## CARD
<img width="1429" height="2000" alt="Ferrari Laferrari" src="https://github.com/user-attachments/assets/5374ccdc-d86c-4779-8824-c7b380921c56" />
This design clearly shows the car name and all state, it is a very simplistic design and synthesizes 0 confusion.
## INTERFACE
SELECTED PLAYER:

CHOOSE YOUR CARD 
+------------------+
|                  |
|                  |
|                  |
|   TOP TARRANTS   |
|                  |
|                  |
|                  |
+------------------+
CHOOSE ATTRIBUTE:
+------------------+      
|     Car Card     |                            
|     Image        |                            
| Top Speed        |                            
| Intelligence     |                            
| Acceleration     |                            
| Strain Gauge     |                            
| Car Type         |                            
| Price            |                            
+------------------+                            

[Top Speed] [Intelligence] [Acceleration]
[Strain Gauge] [Car Type] [Price]

YOU WIN/LOSE

Winner Display
Leaderboard

NON SELECTED PLAYER:
CHOOSE YOUR CARD
+------------------+
|                  |
|                  |
|                  |
|   TOP TARRANTS   |
|                  |
|                  |
|                  |
+------------------+

PLAY ATTRIBUTE
+------------------+      
|     Car Card     |                            
|     Image        |                            
| Top Speed        |                            
| Intelligence     |                            
| Acceleration     |                            
| Strain Gauge     |                            
| Car Type         |                            
| Price            |                            
+------------------+
Selected chose Price

YOU WIN/LOSE
____________________________________________________________________________________________________________________________________________________________________________________________________________________
## PART F: Social, Ethical and Legal Implications
INDIVIDUAL:
1. This game could influence user decision making because players may start to believe that the cars with the highest scores are automatically the "best" cars. Since attributes like Top Speed, Car Intelligence and Price are weighted highly, users may begin favouring expensive or high performance vehicles over practical or affordable options. The game could also encourage some bias. For example a luxury sports car will likely perform much better than an older family vehicle, even though in real life the family vehicle may be more suitable for many people. Players could start associating expensive cars with superiority simply because they win more rounds. As the designer I have a responsibility to present information fairly. This means making it clear that the ratings are only for the game and do not represent the overall quality of a vehicle. I should also make sure that no single attribute becomes too powerful because this could create an unfair advantage and reduce the educational value of the game.
SOCIAL:
2. This game could potentially reinforce social stereotypes regarding wealth and social status because the more expensive cars are rewarded with more points. This may result in players developing the perception that luxury vehicles are automatically superior compared to normal cars, despite this not always being the reality. Due to the fact expensive cars usually have stronger performance statistics they will naturally achieve more victories throughout gameplay. The system also favours certain vehicle demographics over others. Sports cars and newer vehicles generally contain greater technological advancement and performance capabilities meaning they possess a much greater probability of success. Meanwhile practical family vehicles and older cars may not perform as effectively in comparison. This could create an imbalance representation of vehicles. To improve inclusivity I could incorporate additional attributes such as reliability, practicality and fuel economy. This would provide a larger variety of vehicles with opportunities to compete. Furthermore reducing the significance of the price attribute could assist in preventing an unnecessary emphasis on wealth related factors.
ENVIRONMENTAL:
3. The game does consider environmental factors because Hybrid cars receive the most points followed by EV's and then Petrol cars. This could encourage players to think about sustainability and environmentally conscious transport options which is becoming increasingly important in modern society. However at the same time the game still focuses alot on Top Speed and Acceleration. Since these attributes are some of the strongest in the game players may still value performance over environmental sustainability. This creates a bit of a contradiction because the game is promoting both sustainability and high performance at the same time. To improve this I could add attributes such as fuel efficiency or carbon emissions. This would make environmental considerations more significant and provide a more balanced representation of vehicle quality.
LEGAL
4. One legal issue is copyright because vehicle images and information found online usually belong to somebody. This means they cannot simply be copied and used without permission. This is especially important if information or images are taken from websites such as carsales.com.au. Another responsibility is making sure the information is accurate. Vehicle specifications can change depending on the model year or version of the vehicle so incorrect information could mislead players and create unfair comparisons. I also have a responsibility to make it clear that the overall rating is only for gameplay purposes. The rating system is based on a custom formula and does not officially prove one vehicle is better than another vehicle in every situation. 
____________________________________________________________________________________________________________________________________________________________________________________________________________________
## THE END LADS LESSS GOOOOOOOO
<small>no nazi or extremist symbols are present within this task</small>
