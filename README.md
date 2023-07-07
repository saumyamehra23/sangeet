# Music Recommendation Using Deep Learning

Music Recommendation using latent feature vectors obtained from a network trained on the Free Music Archive dataset.

## Overview

The basic idea of this project is to recommend music using computer vision through a convolutional neural network. The network is first trained as a classifier with the labels being the 8 different genres of songs from the dataset. The trained network is then modified by discarding the softmax layer i.e. creating a new model which works as an encoder.

### Dataset
The fma_small dataset consists of 8000 mp3 files from the [Free Music Archive](https://github.com/mdeff/fma).
For testing the recommendation system, I've used 30 songs from my itunes library. I've manually converted the songs into 30 second clips and then I ran my code in *test* mode.

```
30 Seconds To Mars - Night of the hunter (Acoustic)
Afrojack - The spark
Alesso - Heros
Awolnation - Sail
Boyce Avenue - Wonderwall
Bruno Mars - Just the way you are
Bruno Mars - Locked out of heaven
Calvin Harris - Summer
Calvin Harris - Sweet Nothing
Coldplay - Magic
Coldplay - Paradise
Coldplay - Viva La Vida
Coldplay - The Scientist
Daft Punk - Instant crush
Daft Punk - Lose yourself to dance
Don Omar - Danza Kuduro
Enrique Iglesias - Bailando
Imagine Dragons - Demons
Imagine Dragons - It's Time
Jennifer Lopez - On the floor 
John Mayer - Say
Kanye West - Stronger
Katy Perry - Dark Horse
Katy Perry - Fireworks
Khalid - Location
Lana Del Rey - Young and Beautiful
Maroon5 - Moves Like Jagger
Passenger - Let Her Go
Wiz Khalifa - Black and Yellow
Wiz Khalifa - Young, Wild and Free
```

```
['Bailando' 'BlackandYellow' 'DanzaKuduro' 'DarkHorse' 'Demons'
'Fireworks' 'Heros' 'InstantCrush' 'ItsTime' 'JustTheWayYouAre'
'LetHerGo' 'Location' 'LockedOutOfHeaven' 'LoseYourselfToDance' 'Magic'
'MovesLikeJagger' 'NightOfTheHunter' 'OnTheFloor' 'Paradise' 'Sail' 'Say'
'Spark' 'Stronger' 'Summer' 'SweetNothing' 'VivaLaVida' 'Wonderwall'
'YoungAndBeautiful' 'YoungWildAndFree']
```

Enter an anchor song for which you want similar recommendations (Choose one from the above list).
```
Enter a Song Name
The Scientist
```
### Results
The code generates two recommendations for the song The Scientist by Coldplay, 1) Let Her Go by Passenger and 2) Say by John Mayer.

![Output_1](https://github.com/VikramShenoy97/Music-Recommendation-Using-Deep-Learning/blob/master/Images/Output_1.png)
