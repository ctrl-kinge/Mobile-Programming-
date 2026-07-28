# Card Cascade

A mobile Klondike solitaire game built in **Unity 6 (6000.0.41f1)** and **C#**,
for the Mobile Gaming Programming unit at KCA University.

## What it does

Full Klondike solitaire — deal, draw from the stock, build the four foundation
piles by suit, and stack the tableau down in alternating colours. Built for
touch input on mobile.

## How it's put together

| Script | Responsibility |
|--------|----------------|
| [`Solitaire.cs`](Scripts/Solitaire.cs) | Deck construction, shuffle, the initial deal, and the tableau/foundation rules |
| [`Selectable.cs`](Scripts/Selectable.cs) | Per-card state — face up/down, which pile a card belongs to, whether it can be picked up |
| [`UserInput.cs`](Scripts/UserInput.cs) | Touch and click handling, move validation, and card transfer between piles |
| [`ScoreKeeper.cs`](Scripts/ScoreKeeper.cs) | Score and move tracking |
| [`UpdateSprite.cs`](Scripts/UpdateSprite.cs) | Swaps card face and back sprites as cards flip |
| [`UIButtons.cs`](Scripts/UIButtons.cs) | Menu, restart, and navigation buttons |

Playable scene: [`Scenes/SolitaireGame.unity`](Scenes/SolitaireGame.unity).

## Running it

1. Open the project in Unity **6000.0.41f1** or newer (Universal Render Pipeline).
2. Open `Scenes/SolitaireGame.unity`.
3. Press Play, or build for Android via *File → Build Settings*.

## Notes

Card sprites live in `Sprites/`, prefabs in `Prefabs/`. Input is wired through
Unity's Input System (`InputSystem_Actions.inputactions`), so the same build
handles mouse in the editor and touch on device.
