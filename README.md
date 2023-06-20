<img width="500" alt="meme" src="https://github.com/tejxv/spotify-monthly-saves/assets/54097365/2012bdbe-cab7-48d8-98e2-cd4aaf370742">

# Spotify Monthly Saves
Add saved songs to a monthly playlist using GitHub Actions, ditching IFTTT.

### 🧐 What is this?
The songs you add to your library or give a like to will be included in a monthly playlist (e.g., "Jun '23"), enabling you to revisit and discover the songs you liked 7 months ago during a memorable road trip.

Like this:

<img width="280" alt="results" src="https://github.com/tejxv/spotify-monthly-saves/assets/54097365/3e18937d-5937-4f3d-bf00-64c7380eb61d">


### 🗿 Why not [IFTTT](https://ifttt.com/applets/rC5QtGu6-add-saved-songs-to-a-monthly-playlist)?
I have been using that for years, but recently they paywalled it. 🥲
### ✨ How does it work?
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-production-user-asset-6210df.s3.amazonaws.com/54097365/244024820-29c2cff5-84ec-45e5-b6ad-b5447c2494d4.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://github-production-user-asset-6210df.s3.amazonaws.com/54097365/244024165-45dac8e5-66cd-44a0-9284-8d8881938000.svg">
  <img alt="working illustration" src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>


### ⚙️ How do I set it up?

To set up the repository and configure the necessary steps, follow these instructions:

0. Make sure you have a GitHub account. If you don't have one, create an account at [github.com/signup](https://github.com/signup).

1. Fork this repository by clicking the "Fork" button at the top right of the repository page. This will create a copy of the repository under your GitHub account.

2. Obtain your `client_id` and `client_secret` from the Spotify Developer Dashboard:

   - Visit [developer.spotify.com](https://developer.spotify.com/) and log in with your Spotify account.
   - Navigate to your [Dashboard.](https://developer.spotify.com/dashboard)
   - Create a new app by clicking the "Create App" button.
   - Provide a name and description for your app (you can use any name and description).
   - In the Redirect URI field, enter `http://localhost:3000` and click "Save".
   - Open the settings of your app and copy the `client_id` and `client_secret` to a notepad or any text editor. You will need these in the next steps.

3. Before proceeding, make sure you have run the `main.py` file locally with your `client_id` and `client_secret` to authenticate your secret credentials. This step gives the necessary permissions to the app you created, allowing it to modify and create new playlists.

    - Open fork in VS Code
    - ⚠︎ Delete ``.cache`` file (spotify-monthly-saves/.cache)
    - Run ``pip install spotipy``
    - Run the code by pressing <kbd>Control</kbd> + <kbd>Option</kbd> + <kbd>N</kbd> (<kbd>Control</kbd> + <kbd>Alt</kbd> + <kbd>N</kbd> on Windows)
    - A window will pop up asking you to Authorise the Spotify app, click authorise.
4. Go to the "Settings" tab of your forked repository on GitHub, and navigate to "Secrets and variables" > "Actions".

5. Add both the `client_id` and `client_secret` keys as secrets by clicking on "New repository secret" and entering the respective values.

6. Next, enable the workflow under the "Actions" tab by clicking the "I understand my workflows, go ahead and enable them" button. This will allow the automated process to run.

7. Additionally, enable the workflow under the sidebar menu called "Run main.py" by clicking the "Enable workflow" button.

8. Please note that the song you like on Spotify won't be instantly added to the monthly playlist. The GitHub action runs at an interval of approximately 15 minutes, so there might be a slight delay before the song gets added.

9. Once the setup is complete, you can continue to like songs on Spotify, and they will be automatically added to a new monthly playlist during the next execution of the GitHub action.

10. Profit.

### 🧮 Customization

You have the flexibility to customize the interval at which the GitHub Action runs by modifying the `- cron:` parameter in the `.github/workflows/actions.yml` file. The interval is set using the cron syntax.

Cron syntax consists of five fields representing different time units: minute, hour, day of the month, month, and day of the week. Each field can contain specific values or special characters to define the schedule.

To modify the interval, locate the following line in the `.github/workflows/actions.yml` file:

```yaml
- cron: '*/15 * * * *'
```
> this runs every 15 minutes

The `* * * * *` represents the default configuration, which executes the workflow every minute. You can change this to your desired schedule. Refer to [crontab.guru](https://crontab.guru/). It provides a simple and intuitive way to understand and create cron schedules.


### 💰 Is this FREE?
Yes.


