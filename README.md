# ttscli
A CLI Tool that uses curl,jq and ffmpeg with <a href="https://ttsmp3.com">TTSMP3</a> API to convert Text into Speech.

## USAGE
```
ttscli [TEXT_SPEECH]

ttscli 'Text Prompt Here' -p To Play using FFPLAY
ttscli 'Text Prompt Here' -d To Download using FFMPEG
ttscli 'Text Prompt Here' Get the mp3 URL
ttscli -sv | ttscli --show-voices Get list of available voices
ttscli -h | ttscli --help View Help!
```

## PROMPT FEATURES

**Add a break**

Mary had a little lamb `<break time="1s"/>` Whose fleece was white as snow.
Emphasizing words
I already told you I `<emphasis level="strong">really like </emphasis>` that person.

**Speed**

For dramatic purposes, you might wish to `<prosody rate="slow">slow down the speaking rate of your text.</prosody>`
Or if you are in a hurry `<prosody rate="fast">your may want to speed it up a bit.</prosody>`

**Pitch**

Do you like sythesized speech `<prosody pitch="high">with a pitch that is higher than normal?</prosody>`
Or do you prefer your speech `<prosody pitch="-20%">with a somewhat lower pitch?</prosody>`

**Whisper**

`<amazon:effect name="whispered">If you make any noise, </amazon:effect>` she said, `<amazon:effect name="whispered">they will hear us.</amazon:effect>`

**Conversations**

It is possible to switch between speakers within the text. Just use the following format:
[speaker:Brian] Hello Emma
[speaker:Emma] Hey Brian
[speaker:Brian] How are you doing?
[speaker:Emma] I am fine. May i invite you to a cup of tea?

## NOTE

1. Requires Internet To use ttsmp3 API.
2. Maximum Limit of Word is 375 and 3000 Characters.

