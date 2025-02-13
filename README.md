# Dataset-custom-audio
Dataset containing .wav recordings of keyboard presses from a Lenovo IdeaPad Gaming 3. Includes normalized and denoised audio.

# Recording and preprocessing of new audio samples

Following steps of [Audacity](https://support.audacityteam.org/repairing-audio/noise-reduction-removal).

1. Using an iPhone SE 2020 at a distance of 15cm from the bottom right corner of a Lenovo IdeaPad Gaming laptop, audio samples of key presses from the same laptop were recorded. Each audio sample has a duration of around 40 seconds, with 40 presses per audio sample corresponding to the same key. Additionally, a 20-second audio sample of noise was recorded for use in noise removal. The keys were recorded **ABCDEFGHIJKLMNÑOPQRSTUVWXYZ**, in addition to the keys **Space** and **Enter**.   
   1. The Ñ key has the peculiarity that, being an American keyboard, to actually press the “Ñ” key you use the “;” key.  
   2. For display purposes, the Space and Enter keys are denoted during model execution as follows:  
      1. Space key corresponds to \- character.  
      2. Enter key corresponds to \+ character.  
   3. That is, in the model, the set of “keys” worked as labels are the following:
      1. ![All keys available in the dataset.](https://github.com/blondiedies/Dataset-custom-audio/blob/4906a55e9864e79469a8ad4872e49f04b4d5aec2/images/keys_s.png?raw=true)


   The raw audio, displayed in Audacity:
![Spectrogram of raw audio displayed in Audacity.](https://github.com/blondiedies/Dataset-custom-audio/blob/4906a55e9864e79469a8ad4872e49f04b4d5aec2/images/rawaudio.png?raw=true)

2. The audio normalization process (and noise removal) was carried out through the Audacity audio editor. The audio files were loaded and the audio was normalized, with the following configurations: 

![Loudness Normalization presets in Audacity.](https://github.com/blondiedies/Dataset-custom-audio/blob/4906a55e9864e79469a8ad4872e49f04b4d5aec2/images/loudnessnorm.png?raw=true) 
The normalized audio, displayed in Audacity:  
![Spectrogram of normalized audio displayed in Audacity.](https://github.com/blondiedies/Dataset-custom-audio/blob/4906a55e9864e79469a8ad4872e49f04b4d5aec2/images/normalized.png?raw=true)

3. The noise was then removed, using the previously recorded (and normalized) noise sample as the noise profile, with the following settings:

![Noise Reduction presets in Audacity.](https://github.com/blondiedies/Dataset-custom-audio/blob/4906a55e9864e79469a8ad4872e49f04b4d5aec2/images/noisereduce.png?raw=true) 
Noise-free audio, displayed in Audacity:  
![Spectrogram of normalized and noise-removed audio displayed in Audacity.](https://github.com/blondiedies/Dataset-custom-audio/blob/4906a55e9864e79469a8ad4872e49f04b4d5aec2/images/noisereduucedaudio.png?raw=true)

4. Upon completion, three versions of the set of audio files were generated:  
   1. Control version, .wav format, consists of the raw audio.  
   2. Standardized version, .wav format.  
   3. Normalized version and later without noise, .wav format.
