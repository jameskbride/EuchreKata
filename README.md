# The Euchre Kata
## Basic Rules
* Play one hand of Euchre
* 4 Players, 2 teams.  In a real game players sit facing their teammates.
* Even players form one team, odd players form the other team
* Only the 9, 10, J, Q, K, A of each suit (hearts, diamonds, spades, and clubs) are used.  All other cards are excluded from the deck and are not used.
* A hand consists of 5 "tricks"
* In order to win the hand a team must get 3 or more tricks

## Playing a Hand

### Dealing the Hand

_As the Dealer_<br />
_In order to begin the Hand_<br />
_I want to deal each Player their cards_<br />

At the beginning of the hand one player is designated as the dealer, and deals each player 5 cards from the top of a shuffled deck in the following manner: each player gets 2 cards in rotating team order, then each player gets 3 cards in rotating team order.

So:

1. Team 1 Player 1 gets 2 card
2. Team 2 Player 2 gets 2 cards
3. Team 1 Player 3 gets 2 cards
4. Team 2 Player 4 gets 2 cards.  

Next, Team 1 player 1 gets 3 cards, and so on until all 4 players have 5 cards.  

The remainder of the deck (known as the "kitty) is set aside.

### Trump Suit

_As a Player_<br />
_In order to win a Hand_<br />
_I want cards of the Trump Suit to be ranked higher than all other cards_<br />

Cards played from the trump suit are ranked higher than all other cards for the tricks played in that hand.

#### The Right and Left Bars
Cards from the trump suit are ranked from highest to lowest: Right Bar, Left Bar, Ace, King, Queen, 10, 9. The Right Bar is the Jack of the trump suit.  The Left Bar is the Jack of the suit that shares the same color (red or black) as the trump suit.

For example, if Hearts is trump then the ranking of trump cards in descending order would be:
* Jack of Hearts
* Jack of Diamonds
* Ace of Hearts
* King of Hearts
* Queen of Hearts
* 10 of Hearts
* 9 of Hearts

#### Declaring Trump
The "trump" suit is declared at the beginning of the hand, after the cards have been dealt.

After the hand has been dealt the top card of the kitty is turned over by the dealer and each player may get a chance to declare trump for their team in rotating team order.  

If a player:
* has at least three cards of the same suit of the revealed card, or
* has two cards in the revealed suit and an Ace of another suit, or
* is the teammate of the dealer and the player has at least two cards in the revealed suit they should declare trump.  Otherwise they should pass, and the next player in turn gets a chance to declare trump.

Trump may only be declared once, and once declared the remaining players lose their chance to declare it. Once trump is declared the dealer picks up the trump card and discards their lowest card back to the kitty (remember trump cards are higher than all other cards).

If no player declares trump then the hand is over with no winner.

## Playing a Trick
Each hand is played as five tricks (one per card in the hand).  
### Play Order

_As the Players_<br />
_In order to play a Trick_<br />
_We want to play cards in rotating team order_<br />

Each player plays one card per trick. In a real game players play cards clockwise beginning with the player to the left of the dealer. For this exercise players will play their cards in a trick in a fixed, rotating team order. Team 1 Player 1 (assumed to be the player to the left of the dealer) always begins the first trick, so the initial play order would be:
  1. Team 1 Player 1
  2. Team 2 Player 2
  3. Team 1 Player 3
  4. Team 2 player 4

Whoever won the previous trick begins the next trick.  For example, if Team 2 Player 2 won the previous trick then the play order would be:
  1. Team 2 Player 2
  2. Team 1 Player 3
  3. Team 2 Player 4
  4. Team 1 Player 1

### The Lead Suit

_As a Player_<br />
_In order to win a Trick_<br />
_I want the first card played in a Trick to determine the Lead Suit_<br />

The first card played in a trick determines the "lead suit".  Once the lead suit has been determined the other players must "follow suit", meaning if they have a card of that suit they must play it, even if they have trump.  If they don't have a card of the lead suit they may play a trump card or throw "off-suit", meaning play a card which is neither of the lead suit nor trump.  The lead suit may be the trump suit.  

The lead suit is ranked from highest to lowest: Ace, King, Queen, Jack, 10, 9.  If the lead suit is the trump suit then the ranking is based on the trump suit rules.  

If the lead suit is the same color (red or black) as the trump suit but not the same suit, then the Jack of the lead suit is considered to be the Left Bar of the trump suit. Leading with the Left Bar is the same as leading with the trump suit.

### Winning Tricks

_As a Team_<br />
_In order to win a Hand_<br />
_I want to win Tricks_<br />

A trick is complete when all players have played a card.

A trick is won by the player with the highest card played in that trick. The team of the player who won the trick is considered as winning that trick as well.

A player should play a card that will give them the best chance of winning the trick according to the lead suit and trump rules.

Trump cards are higher than the lead suit (if the lead suit is not the trump suit), which is higher than off-suit cards.  Two cards within the same suit should be evaluated by the rules of that suit to determine who wins the trick.

### Wining a hand
_As a Team_<br />
_In order to determine who won the Hand_<br />
_I want to win three or more tricks_<br />

A hand is complete when all five tricks have been played. A hand is won by the team who has three or more tricks.

## Team Play

_As Players_<br />
_In order to win a Hand_<br />
_We want to play as Teams_<br />

Euchre is a team game which is played cooperatively.  Teammates should not work against each other, and should play their cards in a way so as not to waste cards that may let them win a future trick.  

If a teammate appears to be winning a trick then a player should play the lowest card they are allowed to play. On the other hand if a teammate is not winning a trick then a player should play their highest card. Players must still abide by the lead suit and trump rules however.
