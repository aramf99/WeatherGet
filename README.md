# WeatherGet
An API to get any city's weather 
1. Get a free API key — sign up at openweathermap.org/api , grab a key from your account's "API keys" tab. Keys can take up to ~10 minutes to activate.
2. Enter a text input for city name, a "Get Weather" button.

That specific error usually means the request never made it to a response — a few likely causes:
1. No internet connection at the moment of the request — check that first.
2. Ad blocker / privacy extension (uBlock, Brave Shields, Ghostery, etc.) blocking openweathermap.org as a tracker-like domain. Try disabling it for this page, or test in an incognito window with extensions off.
3. Corporate/network firewall or VPN blocking the API domain.
4. Browser blocking file:// fetches — some browsers (especially Safari, and Chrome in stricter modes) restrict fetch() from a page opened directly as a local file. Try opening it through a tiny local server instead:

   cd path/to/folder
   
   python3 -m http.server 8000
   
then visit http://localhost:8000/weather-app.html.

5. Typo in the API key causing a malformed request — double check you pasted it cleanly (no extra spaces).
Quickest diagnostic: open DevTools (F12) → Network tab → try the search again → click the failed request. It'll show whether it's CORS, a blocked request, or DNS/connection failure, which tells us exactly which of the above it is. What do you see there?
