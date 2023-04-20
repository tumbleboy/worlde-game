# Wordle Game
- Players must guess the 5-letter word in 6 total guesses.
- Only 5-letter words are accepted and words that are in the word bank.
    - If you input an invalid guess, this will not use up an attempt.

### Entire program flowchart
```mermaid
 flowchart TD
    A([Start]) --> D[Greeting message]
    D --> B[[Get target word]]
    B --> E[[Prompt for guess]]
    E --> F{Is it valid?}
    F --> |YES| G[[Score guess]]
    F --> |NO| H[Invalid guess message]
    H --> E
    G --> I{Was the word <br/> guessed correctly?}
    I --> |NO| K{Are there still <br/> attempts left?}
    I --> |YES| J[Victory message]
    K --> |YES| E
    K --> |NO| L[Defeat message]
    J --> C[[Play again?]]
    L --> C
    C --> |NO|M([End program])
    C --> |YES|A
    
    
```
