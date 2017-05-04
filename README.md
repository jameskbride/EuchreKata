# The Euchre Kata
## Basic Rules
* Play one hand of Euchre
* 4 Players, 2 teams.  In a real game players sit facing their teammates.
* Even players form one team, odd players form the other team
* Only the 9, 10, J, Q, K, A of each suit (hearts, diamonds, spades, and clubs) are used.  All other cards are excluded from the deck and are not used.
* A hand consists of 5 "tricks"
* In order to win the hand a team must get 3 or more tricks

## Dealing the Hand

_As the Dealer_<br />
_In order to begin the Hand_<br />
_I want to deal each Player their cards_<br />

Each player get 5 cards, dealt from the top of a shuffled deck in the following manner: each player gets 2 cards in rotating team order, then each player gets 3 cards in rotating team order.

So, Team 1 Player 1 gets 2 card, Team 2 Player 2 gets 2 cards, Team 1 Player 3 gets 2 cards, Team 2 Player 4 gets 2 cards.  Next Team 1 player 1 gets 3 cards, and so on until all 4 players have 5 cards.  

The remainder of the deck (known as the "kitty") is discarded and not used. In a real game each player has an opportunity to either choose to make the suit of an upturned card from the top of the kitty "trump" or not after the hand has been dealt.  For the purpose of this exercise assume that this has already been decided.

## Playing a Trick
### Play Order

_As the Players_<br />
_In order to play a Trick_<br />
_I want to play cards in rotating team order_<br />

Each player plays one card per trick. In a real game players play cards clockwise beginning with the player to the left of the dealer. For this exercise players will play their cards in a trick in a fixed, rotating team order. Team 1 Player 1 (assumed to be the player to the left of the dealer) always begins the first trick, so the initial play order would be:
  1. Team 1 Player 1
  2. Team 2 Player 2
  3. Team 1 Player 3
  4. team 2 player 4

Whoever won the previous trick begins the next trick.  For example, if Team 2 player 2 won the previous trick then the play order would be:
  1. Team 2 Player 2
  2. Team 1 Player 3
  3. Team 2 Player 4
  4. Team 1 Player 1

### The Lead Suit

_As a Player_<br />
_In order to win a Trick_<br />
_I want the first card played in a Trick to determine the Lead Suit_<br />

The first card played in a trick determines the "lead suit".  Once the lead suit has been determined the other players must "follow suit", meaning if they have a card of that suit they must play it, even if they have trump (see below).  If they don't have a card of the Lead Suit they may play a trump card or throw "off-suit", meaning a card which is neither of the lead suit nor trump.  The lead suit may be the trump suit.  The lead suit is ranked from highest to lowest: Ace, King, Queen, Jack, 10, 9.  If the lead suit is the trump suit then the ranking is based on the trump suit rules.

### The Trump Suit

_As a Player_<br />
_In order to win a Trick_<br />
_I want cards of the Trump Suit to be ranked higher than all other cards_<br />

The "trump" suit is declared at the beginning of the Hand.  Cards played from this suit will beat all other cards, including the lead suit.

#### The Right and Left Bars
Cards from the trump suit are ranked from highest to lowest: Right Bar, Left Bar, Ace, King, Queen, 10, 9.  The Right Bar is the Jack of the trump suit.  The Left Bar is the Jack of the suit that shares the same color as the trump suit.

For example, if Hearts is trump then the ranking of trump cards in descending order would be:
* Jack of Hearts
* Jack of Diamonds
* Ace of Hearts
* King of Hearts
* Queen of Hearts
* 10 of Hearts
* 9 of Hearts

### Winning a Trick

_As a Team_<br />
_In order to win a Hand_<br />
_I want to win a Trick_<br />

A trick is won by the player with the highest card played in that trick. The team of the player who won the trick is considered as winning that trick as well. Trump cards are higher than the lead suit (if the lead suit is not the trump suit), which is higher than off-suit cards.  Two cards within the same suit should be evaluated by the rules of that suit.
