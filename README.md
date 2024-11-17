# csrd
plying cards
import random

# Define the suits and ranks
suits = ['Hearts', 'Diamonds', 'Clubs', 'Spades']
ranks = ['2', '3', '4', '5', '6', '7', '8', '9', '10', 'Jack', 'Queen', 'King', 'Ace']

# Create a deck of cards
deck = [f"{rank} of {suit}" for suit in suits for rank in ranks]

# Function to shuffle the deck
def shuffle_deck(deck):
    random.shuffle(deck)
    return deck

# Function to draw a card
def draw_card(deck):
    if deck:
        return deck.pop()
    else:
        return "No cards left in the deck!"

# Shuffle the deck
shuffled_deck = shuffle_deck(deck.copy())

# Draw 5 cards as an example
print("Drawing 5 cards from the deck:")
for _ in range(5):
    print(draw_card(shuffled_deck))

# Check how many cards are left in the deck
print(f"\nCards left in the deck: {len(shuffled_deck)}")
