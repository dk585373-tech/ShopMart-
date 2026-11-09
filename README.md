# ShopNest — Full E-Commerce Single Page Application

Built using HTML5, CSS3 and Vanilla JavaScript. Product data comes from public APIs only. There is no local `products.json` file.

## Public APIs
- **DummyJSON Products API:** `https://dummyjson.com/products?limit=100`
  - Supplies product names, prices, discount percentages, ratings and images.
- **Open Library Search API:** `https://openlibrary.org/search.json?q=subject:fiction&limit=12`
  - Supplies book titles and cover IDs.
  - Open Library is a book catalogue, not a retail API. Book prices and ratings in this demo are sample values.

## Features
- Public API requests using Fetch API, async/await and JSON parsing.
- Product data normalized to `id`, `name`, `category`, `price`, `originalPrice`, `rating`, `imageUrl`.
- Product cards created dynamically with DOM methods.
- Live name search using the `input` event.
- Category filters: All, Electronics, Clothing, Footwear, Books.
- Search and category filter work together.
- Add to cart, plus/minus quantity, remove item.
- Reactive cart item count and subtotal.
- Cart saved/restored with localStorage.
- Loading, error/retry and no-results states.
- Responsive desktop, tablet and mobile layout.
- Safe DOM text insertion using `textContent`.

## Run the project
You need an internet connection because product data and images are fetched from public APIs.

### Option 1 — VS Code Live Server
1. Extract the ZIP.
2. Open the `ShopNest-Full` folder in VS Code.
3. Install the **Live Server** extension if it is not installed.
4. Right-click `index.html`.
5. Select **Open with Live Server**.

### Option 2 — Python local server
Open a terminal in this project folder and run:

```bash
python -m http.server 5500
```

Then visit `http://localhost:5500`.

Do not open the HTML directly with `file://`; run it through a local server.

## Folder structure

```text
ShopNest-Full/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── app.js
└── README.md
```

## Assignment checklist
- [x] 12 or more products loaded from public API sources.
- [x] Required product fields present after normalization.
- [x] No hardcoded product cards in HTML.
- [x] DOM methods used for dynamic rendering.
- [x] Live search using input event.
- [x] All five category buttons.
- [x] Search and category filtering combined.
- [x] Add, remove, increase and decrease cart quantity.
- [x] Reactive subtotal and cart count.
- [x] localStorage persistence across refresh.
- [x] No products found message.
- [x] Fetch API with async/await.
- [x] Functions separated by responsibility.
- [x] Loading/error handling and retry button.

## Notes about category mapping and demo values
DummyJSON's catalogue is a general product catalogue and may not include enough products in all the requested retail categories. This demo maps its product categories into the assignment's fixed filter categories. If a true Clothing or Footwear product feed is required, replace or supplement the source with a suitable public catalogue API. Book prices and ratings are placeholders because Open Library does not provide retail prices or product ratings.
