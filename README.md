# Forkify

Forkify is a vanilla JavaScript recipe discovery app. Search a large recipe collection, open a recipe to see its ingredients and directions, adjust ingredient quantities by serving size, and save favorites as bookmarks. You can also submit your own recipes through the app.

## Features

- Search recipes by name or ingredient using the Forkify API.
- Browse search results with pagination.
- View recipe details, cooking time, serving count, ingredients, and source directions.
- Increase or decrease servings and recalculate ingredient quantities.
- Bookmark recipes and keep bookmarks in browser `localStorage` between visits.
- Submit a recipe with its details and ingredients; uploaded recipes are added to bookmarks.
- Use the app layout on desktop and smaller screens.

## Getting started

### Requirements

- Node.js and npm
- A modern browser with an internet connection

### Install and run

```bash
git clone https://github.com/Mrtncod/forkify-app.git
cd forkify-app
npm install
npm start
```

Open the local URL printed by Parcel, usually [http://localhost:1234](http://localhost:1234).

> Run the project through Parcel with `npm start`. Opening `index.html` with VS Code Live Server will not compile the Sass stylesheet or Parcel-specific JavaScript and asset imports, so the app will not render correctly.

## Using the app

1. Enter a recipe or ingredient in the search field and select **Search**.
2. Choose a result to load its details.
3. Use the plus and minus controls beside the serving count to recalculate ingredient amounts.
4. Select the bookmark button on a recipe to save or remove it. Open **Bookmarks** in the header to revisit saved recipes.
5. Select **Add recipe** to submit a recipe. Enter ingredients as `quantity,unit,description`, one ingredient per field. For example: `0.5,kg,Rice` or `1,,Avocado` when no unit is needed.

## API and persistence

Recipe search, recipe details, and recipe submissions use the [Forkify API](https://forkify-api.jonas.io/). An internet connection is needed for those requests. Bookmarks are stored in the current browser using `localStorage`; they are not synchronized between devices or browsers.

## Development

Start Parcel's development server:

```bash
npm start
```

Create an optimized production build:

```bash
npm run build
```

Parcel writes the production site to `dist/`. For Netlify, set the build command to `npm run build` and the publish directory to `dist`.

## Project structure

```text
src/
  img/       Logo, icon sprite, and recipe images
  js/        Application state, API helpers, controller, and views
  sass/      Sass stylesheets
index.html   Application entry point
```

The JavaScript is organized around a model-view-controller pattern: `model.js` manages state and API data, `controller.js` coordinates app actions, and `views/` contains the UI rendering code.

## Built with

- Vanilla JavaScript (ES modules)
- Sass
- Parcel
- Forkify API
- Fraction.js

## Credits

Forkify was created as a learning project based on Jonas Schmedtmann's JavaScript course. The original course project and API provide the recipe app concept and data service.

## License

This project uses the ISC license, as declared in `package.json`.
