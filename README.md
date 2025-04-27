# 🎲 Tenzies Game

[View Live Site](https://celebrated-lebkuchen-d226e1.netlify.app/)

A simple React game where you roll dice until they all show the same number.  
Click a die to "hold" its value between rolls!

---

## 🧠 Key React Concepts I Learned

- **State Management with `useState`**  
  - Managed the list of dice and updated the state immutably using `.map()` and object spreading (`{...die}`).
  - Used lazy initialization (`useState(() => generateAllNewDice())`) to optimize state creation.

- **Referencing DOM Elements with `useRef`**  
  - Used `useRef` to focus the "New Game" button automatically when the user wins.

- **Side Effects with `useEffect`**  
  - Watched the `gameWon` condition and triggered focus when the game is completed.

- **Component Reusability and Props**  
  - Built a reusable `<Die />` component that received props for its value, whether it's held, and a function to toggle hold.
  - Passed event handlers (`hold`) as props.

- **Accessibility Best Practices**  
  - Used `aria-live` to announce winning the game for screen readers.
  - Added `aria-pressed` and `aria-label` attributes to dice buttons for better accessibility.

- **Generating Unique IDs with `nanoid`**  
  - Assigned each die a unique `id` to help React track dice correctly across renders.

- **Conditional Rendering**  
  - Showed confetti when the user wins using `{gameWon && <Confetti />}`.
  - Changed the button text dynamically between "Roll" and "New Game."

---

## 📦 Tech Stack

- React
- Vite (for development/build)
- Netlify (for deployment)

---

## 🏗 How It Works

- You start with 10 random dice.
- Click a die to "hold" its number.
- Press "Roll" to re-roll only the dice that aren't held.
- Keep going until all dice show the same number — and win!

---

## 🚀 Future Improvements

- Add a timer or roll counter.
- Animate dice rolls.
- Save best scores locally.

---

If you liked it, feel free to star 🌟 this project!
