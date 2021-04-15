# Welcome to dword
> An amazing library to create synthetic videos


```python
from dword.core import DeepWord
```

## Installation

1. Install the dword library

```
pip install dword
```

2. Make sure you have [ffmpeg installed.](https://ffmpeg.org/download.html)

## Quick start

### Step 1: Use api keys to login

Start by [logging into your DeepWord account](https://login.deepword.co/user/signin) and generating API keys

![test_image](images/api_key.png)

Use these keys to login to your account in Python

```python
acc = DeepWord(API_KEY, SECRET_KEY)
```

### Step 2: Start creating videos

**That's it!!!** Now you can start creating videos. We have many options for choosing a video or an audio. Possible pipelines for each is shown below

## Pipelines for videos

The main function in ``dword`` is the ``generate_video`` function. It's what we will use to generate synthetic videos. All we need is a video of the person we want talking and the audio we want them to say.

For the video, we have 3 options
### Option 1: Local video file

You can have a file downloaded locally. In that case you just need to pass the path to the file to the ``generate_video`` function

```python
acc.generate_video('videos/local_vid.mp4', audio, outfile)
```

### Option2: YouTube video

You can use a YouTube video as the input to the generate video function. For this, you will have to first download the YouTube video and then use it as a local video like we did in the example above. For this, we will use the ``download_youtube_video`` function. You can also provide a start_time and an end_time to crop the video before downloading

```python
url = 'https://youtu.be/QNE2bmCuhMY'
acc.download_youtube_video(url = url)
```

```python
# acc.download_youtube_video(url, start_time="00:00:01", end_time="00:00:03")
```
