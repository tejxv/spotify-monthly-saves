<img width="500" alt="meme" src="https://github.com/tejxv/spotify-monthly-saves/assets/54097365/2012bdbe-cab7-48d8-98e2-cd4aaf370742">

## Spotify Monthly Saves
Add saved songs to a monthly playlist using GitHub Actions.

### 🧐 What is this?
![results](https://github.com/tejxv/spotify-monthly-saves/assets/54097365/3e18937d-5937-4f3d-bf00-64c7380eb61d)

The songs you add to your library or give a like to will be included in a monthly playlist (e.g., "Jun '23"), enabling you to revisit and discover the songs you liked 7 months ago 
during a memorable road trip.

### 🗿 Why not [IFTTT](https://ifttt.com/applets/rC5QtGu6-add-saved-songs-to-a-monthly-playlist)?
I have been using that for years, but recently they paywalled it. 🥲
### ✨ How does it work?
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-production-user-asset-6210df.s3.amazonaws.com/54097365/244024820-29c2cff5-84ec-45e5-b6ad-b5447c2494d4.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://github-production-user-asset-6210df.s3.amazonaws.com/54097365/244024165-45dac8e5-66cd-44a0-9284-8d8881938000.svg">
  <img alt="working illustration" src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>


### ⚙️ How do I set it up?
1. Fork this repository.
2. Get your ``client_id`` and ``client_secret`` from [developer.spotify.com](https://developer.spotify.com/)
    - Create new app by pressing [create app](https://developer.spotify.com/dashboard/create) button.
    - Give it a name, description and type ``http://localhost:3000`` in Redirect URI then click save.
    - Open the settings of the app and copy the ``client_id`` and ``client_secret``.
3. Open forked repo's settings tab > Secrets and variables > Actions.
4. One by one, add both of the keys here by clicking on ``New repository secret``
5. Like a song and it should get added to a new monthly playlist.
6. Profit?
