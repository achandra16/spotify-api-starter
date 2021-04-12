## Setup
#### Register Your Application With Spotify
In order to access certain features of the Spotify Web API, we need to tell spotify that we're a legitimate app.
To do this, go to https://developer.spotify.com/my-applications and create a new Application.

For the Redirect URI, add `http://localhost/` - It should look like this:
![spotify application page](https://raw.githubusercontent.com/markkohdev/spotify-api-starter/master/assets/spotify_api.png)

From that page, copy your ClientId and your ClientSecret and put them into a file called
`credentials.sh` in the root of this repo that looks like this:
```
export SPOTIPY_CLIENT_ID='your-spotify-client-id'
export SPOTIPY_CLIENT_SECRET='your-spotify-client-secret'
export SPOTIPY_REDIRECT_URI='http://localhost/'
```
For details about how the API authenticates your account with this, see
https://developer.spotify.com/web-api/authorization-guide/#authorization_code_flow

#### Install Dependencies
In order to run this program, we need to make sure python3, pip, and virtualenv are installed on your system.
To install this stuff, run
```
./setup.sh
source ~/.bashrc
```

## Completing the Code
Some parts of the project have been removed so you can complete them yourself. These parts are at lines:
* *src/common.py*
    1. line 78
    2. line 91
* *src/display_utils.py*
    1. line 33
    2. line 48
    3. line 104
* *src/main.py*
    1. line 103

You can complete these tasks using the skills you learned in this course, like loops, dictionaries, function calls, and lists (among others). Once you have completed these, you can run the project!


## Running
Simply run
```
make run
```

Once the program runs, you'll be prompted for your username, and your browser window will open.
Once you log in with Spotify, **you will be redirected to a 404 page - THIS IS TOTALLY FINE.**  Copy the URL that you're
redirected to and paste it into the terminal.

After that, just follow the terminal :)

#### Example Run
```
**************************************************
Spotify Web API Demo App
**************************************************
    Let's get some audio features!
    Would you like to:
      1.) Search for a song
      2.) Choose from your playlists
      3.) Pick from your saved songs
Choice: 2

What is your Spotify username: markster3910


            User authentication requires interaction with your
            web browser. Once you enter your credentials and
            give authorization, you will be redirected to
            a url.  Paste that url you were directed to to
            complete the authorization.


Opened https://accounts.spotify.com/authorize?client_id=...


Enter the URL you were redirected to: http://localhost/callback?code=...



******************************
Your Playlists
******************************
  1) An Album a Day Keeps the Doctor Away - spotify:user:markster3910:playlist:5Exd8CXJ9NSrUWhd1iMwXI
  2) Swingin' Electro - spotify:user:markster3910:playlist:2iu5E2EZgfNroIFFzxIyas
  3) Gramatik & Friends - spotify:user:markster3910:playlist:0JrrAohiYpRNYpduglGBZi

Choose a playlist: 1

**************************************************
Tracks in "An Album a Day Keeps the Doctor Away"
**************************************************

  1) Spanish Key - Miles Davis
  2) John McLaughlin - Miles Davis
  3) Miles Runs the Voodoo Down - Miles Davis
  4) Sanctuary - Miles Davis
  5) She Ain’t Right For You - Macy Gra
  6) Waterwheel - Oregon
  7) Witchi-Tai-To - Oregon
  8) El Tren de la Vida - Perujazz, Abraham Laboriel, Alex Acuña
  9) Whoodeeni - De La Soul, 2 Chainz
  10) Nosed Up - De La Soul
  11) You Go Dave (A Goldblatt Presentation) - De La Soul, David Goldblatt

Choose some tracks (e.g 1,4,5,6,10): 1,7,10

******************************
Audio Features
******************************

  Spanish Key - Miles Davis
    tempo: 106.711
    time_signature: 4
    key: D
    loudness: -7.175
    energy: 0.785
    dancibility: None
    acousticness: 0.489
    instrumentalness: 0.411
    liveness: 0.121
    speechiness: 0.0542

  Witchi-Tai-To - Oregon
    tempo: 146.625
    time_signature: 4
    key: D
    loudness: -17.951
    energy: 0.318
    dancibility: None
    acousticness: 0.657
    instrumentalness: 0.758
    liveness: 0.183
    speechiness: 0.036

  Nosed Up - De La Soul
    tempo: 92.293
    time_signature: 4
    key: C♯/D♭
    loudness: -12.567
    energy: 0.458
    dancibility: None
    acousticness: 0.0835
    instrumentalness: 1.97e-05
    liveness: 0.552
    speechiness: 0.335

Run the program again? (Y/N): n
```
