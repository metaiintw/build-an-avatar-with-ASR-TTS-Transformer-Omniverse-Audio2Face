# Build an avatar with ASR, Sentence-transformer, Similarity Search, TTS and Omniverse Audio2Face
## Project Description
I'll show you how I used several Python packages and NVIDIA's Omniverse Audio2Face to quickly implement an avatar that can answer questions defined in a knowledge set or FAQ.

## Demo
[![IMAGE ALT TEXT](https://user-images.githubusercontent.com/104120636/166487700-9f14813c-13b9-42bc-b477-c0f8aff7db5d.png)](http://www.youtube.com/watch?v=G_c94cGIKgs "Video Title")


## How It Works
![](https://i.imgur.com/BZIBUAt.png)
#### ***Automatic Speech Recognition, ASR***
Upon receiving user's request, the [SpeechRecognition API](https://pypi.org/project/SpeechRecognition/) records the frequencies and sound waves from user's voice and translates them into text. 
#### ***Language Understanding***
[Sentence-Transformer](https://www.sbert.net/) is for state-of-the-art sentence, text and image embeddings that can encode input questions into feature vectors. The feature vectors represent entire sentences and their semantic information, this helps the machine in understanding the context, intention, and other nuances in the entire text.

We’ll conduct a similarity search, comparing a user input question to a list of FAQs and return the most likely answers by [Facebook’s Similarity Search API](https://ai.facebook.com/tools/faiss/).
#### ***Text To Speech***
The avatar's voice is fully synthesized by the [Gtts API](https://pypi.org/project/gTTS/), which turns text into natural-sounding speech. The synthesized voice is also used to drive the avatar's facial animation.
#### ***Omniverse Audio2Face***
![](https://i.imgur.com/7ioYQHj.png)

Omniverse Audio2Face is an application brings our avatars to life. With [Omniverse Audio2Face](https://www.nvidia.com/en-us/omniverse/apps/audio2face/), anyone can now create realistic facial expressions and emotions to match any voice-over track. The technology feeds the audio input into a pre-trained Deep Neural Network, based on NVIDIA and the output of the network drives the facial animation of 3D characters in real-time.
## System Requirements
|  Element   | Minimum Specifications |
|  ----  | ----  |
| OS Supported	  | 	Windows 10 64-bit (Version 1909 and above) |
| CPU  | 	Intel I7, AMD Ryzen 2.5GHz or greater |
| CPU Cores  | 	4 or higher |
| RAM  | 	16 GB or higher |
| Storage  | 	500 Gb SSD or higher |
| GPU  | 	Any RTX GPU |
| VRAM  | 	6 GB or higher |
| Min. Video Driver Version  | 	See latest drivers [here](https://developer.nvidia.com/omniverse/driver) |
## How to Install and Run the Project
Before you begin, you'll need to clone the repository with the template code used in this repo. Open your Terminal app and find a directory where you'd like to store the code. Run this command to clone the GitHub App template repository:

```
$ git clone https://github.com/metaiintw/build-an-avatar-with-ASR-TTS-Transformer-Omniverse-Audio2Face.git
```
#### Creating an environment from an environment. yml file
Make sure Anaconda is installed on your local machine. Use the following command to install packages included in requirements.yml:
```
$ conda env create -f /path/to/requirements.yml
```
#### Download and Install Omniverse Launcher
[NVIDIA Omniverse](https://docs.omniverse.nvidia.com/prod_install-guide/prod_install-guide.html) is a development platform for 3D simulation and design collaboration, it is free for individual, you can download Omniverse Launcher [here](https://www.nvidia.com/en-us/omniverse/download/).

I also recommend you to watch this [video tutorial](https://www.youtube.com/watch?v=Ol-bCNBgyFw), which guides you through the installation process. 

| ![](https://i.imgur.com/4imNFt1.jpg) | 
|:--:| 
| *Omniverse Launcher* |

#### Install Omniverse Audio2Face
| ![](https://i.imgur.com/6kbTCRW.jpg) | 
|:--:| 
| *Omniverse apps* |

Once you got Omniverse Launcher installed, you can immediate access to all the apps, including [Omniverse Audio2Face](https://www.nvidia.com/en-us/omniverse/apps/audio2face/). Next, simply install Omniverse Audio2Face and you're good to go.

| ![](https://i.imgur.com/N94KDTc.png) | 
|:--:| 
| *Omniverse Audio2Face* |

#### Omniverse Audio2Face setup
To get our Python program interacts with Omniverse Audio2Face, you should use streaming audio player that allows developers to stream audio data from an external source or applications via the gRPC protocol. 

| ![](https://i.imgur.com/qZUQVS0.png) | 
|:--:| 
| *streaming audio player allows developers to stream audio data from an external source* |

This [tutorial](https://www.youtube.com/watch?v=qKhPwdcOG_w&t=17s) showcases how to create an audio player and connect it to the audio2face instance using the omnigraph editor.
#### Bring Your Avatar to life
Now we're ready to bring our avatar to life, simply enter the following commands into your terminal. 
```
$ cd path_to_the_project_folder
$ conda activate avatar
$ jupyter lab
```
Execute the .ipynb notebook file named  ***1.Creating_a_simple_avatar.ipynb***, start building your first avatar!

| ![](https://i.imgur.com/YTSdxJT.png) | 
|:--:| 
| *1.Creating_a_simple_avatar.ipynb* |

## Creators

**Renton Hsu**

- [Linkedin](https://www.linkedin.com/in/renton-hsu-bba5a0102)
- [Facebook](https://www.facebook.com/renton.hsu/)





