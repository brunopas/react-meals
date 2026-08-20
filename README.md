# ReactMeals

Order meals from a React cart UI backed by Firebase Realtime Database. Study project from the [React - The Complete Guide](https://www.udemy.com/course/react-the-complete-guide-incl-redux/) course by Maximilian Schwarzmuller on Udemy.

## Features

- Browse a list of available meals fetched from Firebase
- Add and remove items from a cart with live totals
- Checkout form with name, street, postal code, and city validation
- Submit orders to Firebase Realtime Database
- Animated cart button badge

## Tech stack

- **Framework:** React 18 (Create React App)
- **State management:** React Context API + `useReducer`
- **Backend:** Firebase Realtime Database (REST)
- **Styling:** CSS Modules

See [package.json](./package.json) for full dependency list.

## Requirements

- [Node.js](https://nodejs.org/) 18 or later
- [Git](https://git-scm.com/)
- A [Firebase](https://firebase.google.com/) project with Realtime Database enabled

## Environment variables

Copy `.env.example` to `.env` and set:

| Variable | Required | Description |
| --- | --- | --- |
| `REACT_APP_FIREBASE_URL` | Yes | Firebase Realtime Database URL (e.g. `https://your-project-default-rtdb.firebaseio.com`) |

## Getting started

```bash
git clone https://github.com/brunopas/react-meals.git
cd react-meals

npm install
cp .env.example .env
# Fill in your Firebase URL in .env

npm start
```

Open [http://localhost:3000](http://localhost:3000).

## Scripts

| Command | What it does |
| --- | --- |
| `npm start` | Start the development server |
| `npm run build` | Create a production build |
| `npm test` | Run tests |

## Project structure

```text
react-meals/
├── public/                  # Static HTML, favicon, manifest
└── src/
    ├── assets/              # Hero image (meals.jpg)
    ├── components/
    │   ├── Cart/            # Cart, CartItem, Checkout, CartIcon
    │   ├── Layout/          # Header, HeaderCartButton
    │   ├── Meals/           # AvailableMeals, MealItem, MealsSummary
    │   └── UI/              # Card, Input, Modal (reusable)
    ├── store/               # CartProvider, cart-context (Context + useReducer)
    ├── App.js               # Root component
    └── index.js             # Entry point
```

## License

MIT. See [LICENSE](./LICENSE).
