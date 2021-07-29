## 7.6 Inheritance VS Composition

Inheritance provides an alternative to composition as a design approach to deal with situations 
where some objects are "extended" versions of another.

Let's consider the composition vs. inheritance alternatives for meeting the requirements for a `MemorizingDeck`

With composition, we can define a class `MemorizingDeck` that implements `CardSource` but *aggregates* a simple deck.

The methods of `MemorizingDeck` will then *delegate* their call to the methods on the `Deck` object.

```java

public class MemorizingDesk implements CardSourcee {
  private final CardStack aDrawCards = new CardStack();
  private final Deck aDeck = new Deck();
  public boolean isEmpty() { 
    return aDeck.isEmpty(); 
  }

  public void shuffle() {
    aDeck.shuffle();
    aDrawnCards.clear();
  }
  
  public Card draw() {
    Card card = aDeck.draw();
    aDrawnCard.push(card);
    return card;
  }
}
```

In contrast, with inheritance, the cards in the deck are not stored in a separate deck, but rather referred to form a field *inherited* from the superclass. In terms of methods, `shuffle()`, `isEmpty()`, and `draw()` are also inherited from the superclass, so they do not need to be redefined to delegate the call, as in composition. 

In our example, we only need to override `shuffle()` and `draw()` to account for the memorization. Method `isEmpty()` can be directly inherited and still do what we want. In the code of the overridden methods, the delegation to another object is replaced by a super call, which executes on the *same* object. 
