Netflix Rating Injector — Tampermonkey Userscript

A lightweight Tampermonkey script that automatically fetches IMDb ratings for movies and series and injects them directly into Netflix title cards.
No more switching tabs — browse Netflix with ratings visible in real-time.

🚀 Features

✔ Automatically detects Netflix movies & shows

✔ Scrapes the title name from Netflix’s HTML structure

✔ Fetches IMDb rating using the OMDb API

✔ Injects a clean badge into each title card

✔ Works on all Netflix pages (Home, Search, Categories)

✔ Efficient: Uses MutationObserver for dynamic loading

✔ Customizable badge styling

🛠 Requirements

Browser: Chrome, Firefox, Edge

Extension: Tampermonkey

API Key: OMDb API key

📥 Installation

Install Tampermonkey extension.

Click "Create a new script" in Tampermonkey.

Copy & paste the script file (netflix-rating-injector.user.js).

Replace the API key inside the script:
const OMDB_API_KEY = "YOUR_OMDB_KEY"; 

Save the script.

Open Netflix.com and watch ratings appear.

🔍 How It Works

The script continuously watches Netflix’s DOM using a MutationObserver.

Every time a title card appears, the script:

Extracts the movie/show title (from the <img alt=""> or fallback text)

Calls the OMDb API:
https://www.omdbapi.com/?t=<TITLE>&apikey=<KEY>
Example HTML Target

The script attaches the rating badge to components like:
<div class="title-card-container">
   <div class="title-card">
      <img alt="Genie, Make a Wish">
   </div>
</div>
Limitations

Netflix sometimes uses non-standard titles → rating may not match

OMDb may return "N/A" for unreleased or regional content

Requires active network access

Badges may overlap in very small thumbnails

🧭 Roadmap

Planned additions:

Rotten Tomatoes + Metacritic scores

Rating overlays on hover

Local caching for faster loading

Settings panel for userscript options

🤝 Contributing

Feel free to submit pull requests or feature ideas.

