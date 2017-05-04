# The Euchre Kata
[Euchre](https://en.wikipedia.org/wiki/Euchre) is a trick-based, team-based card game popular in parts of the Midwest.  It implements a relatively simple set of rules, and is played for points across multiple hands. This kata implements a set of abbreviated rules of Euchre for a single hand. Some rules, such as the second round of declaring trump, going it alone, and partner's best will not be implemented here.

The point of this kata to to provide a larger than trivial exercise that can be used to practice TDD. A significant portion of the effort will be in determining what tests should be written and, more importantly, written next.

## Basic Rules

Euchre has four players split into two teams. Teammates sit facing each other, and game play is always in rotating team order in clockwise fashion. Only the 9, 10, Jack, Queen, King, and Ace of the deck are used for each suit (hearts, diamonds, spades, and clubs).  All other cards are excluded from the deck and are not used.

## Playing a Hand

### Dealing

_As the Dealer_<br />
_In order to begin the Hand_<br />
_I want to deal each Player their cards_<br />

At the beginning of the hand one player is designated as the dealer, who deals each player 5 cards from the top of a shuffled deck.  Cards are dealt in 2 rounds; in the first round all players get 2 cards, and in the second round all players get 3 cards.

The remainder of the deck (known as the "kitty") is set aside.

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

After the hand has been dealt the top card of the kitty is turned over by the dealer and each player may get a chance to declare trump for their team in rotating team order, with the dealer choosing last.  

If a player:
* has at least three cards of the same suit of the revealed card, or
* has two cards in the revealed suit and an Ace of another suit, or
* is the teammate of the dealer and the player has at least two cards in the revealed suit

they should declare trump.  Otherwise they should pass, and the next player in turn gets a chance to declare the revealed suit as trump.

Trump may only be declared once, and once declared the remaining players lose their chance to declare it. Once trump is declared the dealer picks up the trump card and discards their lowest card back to the kitty (remember trump cards are higher than all other cards).

If no player declares trump then the hand is over with no winner.

## Playing a Trick
Once trump has been declared the hand is played as a series of five tricks (one per card in the hand).

### Play Order

_As the Players_<br />
_In order to play a Trick_<br />
_We want to play cards in rotating team order_<br />

Each player plays one card per trick. The player to the left of the dealer plays the first card of the first trick. Whoever won the previous trick begins the next trick, followed by the rest of the players in rotating team order.  

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

### Winning a hand
_As a Team_<br />
_In order to determine who won the Hand_<br />
_I want to win three or more tricks_<br />

A hand is complete when all five tricks have been played. A hand is won by the team who has three or more tricks.

## Team Play

_As Players_<br />
_In order to win a Hand_<br />
_We want to play as Teams_<br />

Euchre is a team game which is played cooperatively.  Teammates should not work against each other, and should play their cards in a way so as not to waste cards that may let them win a future trick.  

In a real game this is where human strategy is involved.  For the purpose of this exercise if a teammate appears to be winning a trick then a player should play the lowest card they are allowed to play. On the other hand if a teammate is not winning a trick then a player should play their highest card if it will beat the opposing team's cards.  If the player's team is not winning, and their highest card can't win either then they should play their lowest card. Players must still abide by the lead suit and trump rules.  
