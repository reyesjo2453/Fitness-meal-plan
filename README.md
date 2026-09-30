# FitTrack

FitTrack is a mobile-friendly food diary for tracking calories, macros, fiber, body weight, and homemade recipes. It runs in your browser and saves your diary on that device.

## What you can do

- **Log meals by day:** Add foods to Breakfast, Lunch, Dinner, or Snacks; adjust quantities and units; edit, copy, or delete entries.
- **Find foods:** Search Open Food Facts and the USDA food database, scan a packaged food's barcode, or enter its nutrition manually.
- **Use AI when you choose:** Describe a meal or take a photo to get an estimated food entry. This requires your own Gemini API key.
- **Build recipes:** Add ingredient rows manually with no API key, or optionally use AI or scan a product barcode. Enter each ingredient's amount and nutrition, set the number of servings, preview nutrition per serving, and save the recipe for quick logging later. Batch totals can also be entered manually.
- **Track goals and trends:** Set daily calorie, carb, protein, fat, and fiber goals; record weight; see a daily dashboard and 7- or 14-day charts.
- **Back up your data:** Export a JSON backup and import it on another browser or device.

## Get started

1. Open the app's `index.html` from a web host in a current browser. For camera scanning on a phone, use an HTTPS address and allow camera access when prompted.
2. Open **Dashboard** to set your calorie and nutrition goals.
3. In **Diary**, choose a date and add a food under the meal you want to log. Search, scan, describe a meal, take a photo, use a saved recipe, or enter nutrition manually. Check the values and tap **Save Entry**.
4. To make a recipe, open **My Recipes** from the food entry screen and choose to create one. Add ingredients manually, with optional AI or barcode help; set servings; review the per-serving preview; and save it. Select the recipe to add it to the diary.

For AI features, enter a Gemini API key in **Dashboard → Settings & Goals**. Direct food logging, manual ingredient entry, manual recipe totals, and goals work without an AI key. Barcode lookup and food search require internet access and depend on the availability of their food databases.

## Get a Gemini API key for the optional AI features

1. Sign in to [Google AI Studio's API Keys page](https://aistudio.google.com/api-keys) with a Google account and accept the terms if prompted.
2. Copy the key shown for your default project, or select **Create API key** and copy the new key. Google's [API key guide](https://ai.google.dev/gemini-api/docs/api-key) has the current steps.
3. In FitTrack, open **Dashboard → Settings & Goals**, paste the key into **Gemini API Key**, and leave the field to save it. Then try describing a meal or adding recipe ingredients with AI.

Google offers a [free Gemini API tier](https://ai.google.dev/gemini-api/docs/pricing) for supported models, subject to usage limits. Check that your project is on the **Free** plan in AI Studio before using the key; enabling billing or switching to a paid project can incur charges. Keep the key private. FitTrack stores it in this browser and includes it in exported backups, so do not share those backups or paste the key into your repository. This browser-based app sends requests directly to Google's API; use a separate, restricted key for personal use and avoid entering a sensitive or paid-project key on a shared device.

## Data and accuracy

Your diary, recipes, goals, weight records, and Gemini API key are stored in this browser's local storage. They do not automatically sync across devices. Export a backup regularly, especially before clearing browser data or changing devices. **The exported JSON includes your API key**, so keep backup files private.

Nutrition returned by AI or public food databases may be incomplete or inaccurate. Check labels and ingredient amounts before saving, especially when building a recipe. A barcode lookup may not find every product.

## About the app

FitTrack is a single-page HTML app in `index.html`. It uses browser storage rather than an account or server. Its interface loads Tailwind CSS, Chart.js, Font Awesome, and the html5-qrcode scanner from CDNs. Food lookup uses Open Food Facts and the USDA FoodData Central search API; optional AI requests go to Google's Gemini API using the key entered in the app.

## ChatGPT connection (optional)

Use **Sync with ChatGPT** in the app's settings to send a snapshot to [Fitness Connect](https://fitness-connect.reyesjo2453.chatgpt.site). Sign in, review the incoming record counts, and select **Save synced records**. If the new window cannot receive the records, export a JSON backup from this app and upload it at Fitness Connect instead.

Install and connect the personal **Fitness Connect** plugin in ChatGPT to read your synced records. The connection supports nutrition summaries, meals, recipes, weight history, completed workouts, personal records, and recovery estimates. It cannot modify your app records. Sync again after changes; ChatGPT reads the last synced copy. Only the owner's account can access this personal connection, and Gemini API keys are excluded from stored snapshots.
