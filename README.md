# groupImg

A python script to organize your images by similarity.

It uses a [k-means](https://en.wikipedia.org/wiki/K-means_clustering) algorithm to separatem them in clusters.

Watch it working below.

[![groupImg](http://img.youtube.com/vi/LgzsJU-b34o/0.jpg)](http://www.youtube.com/watch?v=LgzsJU-b34o)

## Why ?

It was about one year since I made the switch from Windows to Linux, and I wanted to get better at the terminal. I always thought it was cool to master it. To make a long story short, one day I did mount a linux image on my external backup drive instead of the pen drive. Some basic */dev/sd\** confusion. Anyway's, I overwrited all my photos; so I used [Foremost](https://en.wikipedia.org/wiki/Foremost_(software)) (which is a great tool) to recover them. It recover 350.000 photos. So I wrote a little script to divide them in folders, 1000 photos per folder, if I'm not mistaken. I went through all the folders selecting the ones that were important from the ones that weren't. To end the story, I came up with this script to "cluster" the photos by similiraty and makes things a little easier for me.

## How to use

Install the requirements.txt

```
pip install -r requirements.txt
```

Add the *groupimg* to your scripts folder and give it execute permission.

Call the script passing the image folder you want to organize.

```
groupimg -f /home/user/Pictures/
```

## Parameters

\-f folder where your images are (use absolute path).
```groupimg -f /home/user/Pictures```

\-k number of folders you want to separate your images. 
```groupimg -f /home/user/Pictures -k 5```

\-m if you want to move your images instead of just copy them.

\-s if you want the algorithm to consider the size of the images as a feature.

## To Do

Add multiprocessing

Rewrite how the script handles the OS calls (find images, navigate to folders...)

Add new ways to break down the image as features

Test it cross platform

resample the image before processing it
