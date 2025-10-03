# Details
One can find the slides of lecture 2 `Lecture 2.pdf`.
 
Below one can find the first exercises for the Digital Signal Processing part of Introduction to Smart Systems Engineering course at the Hanze University of Applied Sciences.


# Exercises

1. Using Python download a sound file and load it into Python. Plot the data in the time domain. You can use this code to obtain a sound file:

```python
import urllib.request
import librosa
from IPython import display

file_name = "2776.mp3"  # Source: https://bigsoundbank.com/detail-2776-cockatiel-parakeet-8.html
url = f"https://bigsoundbank.com/UPLOAD/mp3/{file_name}"

urllib.request.urlretrieve(url, file_name)
sound_data, samplerate = librosa.load(file_name)  # sr=None keeps the original sample rate
print(samplerate)

display.display(display.Audio(data=sound_data, rate=samplerate))
```

1. Using this documentation: https://docs.scipy.org/doc/scipy/tutorial/fft.html find out how to convert the sound file into the frequency domain, implement this on your data. Plot it in the frequency domain.

1. What can you learn from this plot? Analyze it.

1. Repeat the exercise with a different sound, compare the two different frequency domain plots.

1. Extra challenge, instead of relying on the Fast Fourier Transform, can you implement your own Discrete Fourier Transform?
