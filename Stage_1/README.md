# Mental_Health_Digital_Twin
Text Pipeline

The following features are extracted from the journal:

Feature	Size

SBERT Embedding	384

Emoiton Detection Model	28

VADER Sentiment	7

Lexical Diversity	2

Readability	3

First Person Pronouns	2

Length Features	3

Punctuation Features	4

Time Metadata	3

Health Features + Masks	8

Total text features = 444

Audio Pipeline (Optional)

If an audio file is provided:

Whisper-Speech transcription

Language detection

Word timestamps

Acoustic Features (7)--

Speech rate

Pause ratio

Average pause length

Mean pitch

Pitch variation

Mean loudness

Loudness variation

Speech Emotion Recognition (4)

Using superb/wav2vec2-base-superb-er(A pretrained model)

Angry

Happy

Neutral

Sad

Audio feature mask (11) is also added to indicate whether audio was available.

Final Feature Vector
Text Features        : 444
Audio Features       : 11
Audio Feature Mask   : 11
----------------------------
Total                : 466

If no audio is provided, the audio features are replaced with zeros and the mask is set to 0, keeping the output size fixed.
