# FitTrack

FitTrack is a mobile-friendly food diary for tracking calories, macros, fiber, body weight, and homemade recipes. It runs in your browser and saves your diary on that device.

## What you can do

- **Log meals by day:** Add foods to Breakfast, Lunch, Dinner, or Snacks; adjust quantities and units; edit, copy, or delete entries.
- **Find foods:** Search Open Food Facts and the USDA food database, scan a packaged food's barcode, or enter its nutrition manually.
- **Use AI when you choose:** Describe a meal or take a photo to get an estimated food entry. This requires your own Gemini API key.
- **Build recipes:** Add ingredients from an AI description or scan a product barcode (you can also type its barcode). Review and edit each ingredient's amount and nutrition, set the number of servings, preview nutrition per serving, and save the recipe for quick logging later. You can enter recipe totals manually as well.
- **Track goals and trends:** Set daily calorie, carb, protein, fat, and fiber goals; record weight; see a daily dashboard and 7- or 14-day charts.
- **Back up your data:** Export a JSON backup and import it on another browser or device.

## Get started

1. Open the app's `index.html` from a web host in a current browser. For camera scanning on a phone, use an HTTPS address and allow camera access when prompted.
2. Open **Dashboard** to set your calorie and nutrition goals.
3. In **Diary**, choose a date and add a food under the meal you want to log. Search, scan, describe a meal, take a photo, use a saved recipe, or enter nutrition manually. Check the values and tap **Save Entry**.
4. To make a recipe, open **My Recipes** from the food entry screen, choose to create a recipe, add ingredients, set servings, review the per-serving preview, and save it. Select the recipe and then save the resulting diary entry.

For AI features, enter a Gemini API key in **Dashboard → Settings & Goals**. Food logging, manual recipes, and goals work without an AI key. Barcode lookup and food search require internet access and depend on the availability of their food databases.

## Data and accuracy

Your diary, recipes, goals, weight records, and Gemini API key are stored in this browser's local storage. They do not automatically sync across devices. Export a backup regularly, especially before clearing browser data or changing devices. **The exported JSON includes your API key**, so keep backup files private.

Nutrition returned by AI or public food databases may be incomplete or inaccurate. Check labels and ingredient amounts before saving, especially when building a recipe. A barcode lookup may not find every product.

## About the app

FitTrack is a single-page HTML app in `index.html`. It uses browser storage rather than an account or server. Its interface loads Tailwind CSS, Chart.js, Font Awesome, and the html5-qrcode scanner from CDNs. Food lookup uses Open Food Facts and the USDA FoodData Central search API; optional AI requests go to Google's Gemini API using the key entered in the app.
