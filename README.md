## Core shell functions for AI 

## What is **AIyu**:
In essence, the Aiyu Shell pipelines serve as the interweaving adhesive that binds the various AI components together - a technological superglue of sorts!

**Aiyu** allows to build pipelines that easlily leverage the most exciting **ai** technologies using any laptop.

#### example

###### input:  audio in some language; output: audio in French
```
m2a; a2a fr; a2sk
```
Listen to your microphone and outputs an audio file (m2a), then use the previously created audio and translate it to French (a2a fr) and lastly plays the audio to your speaker (a2sk). 


###### input: audio question in some language; output: audio GPT response in Italian
```
m2a; a2p; p2a; a2a it 
```
Listen to your microphone and outputs an audio file (m2a), then use the created audio and transcribes it to textual prompt (a2p), use the prompt to query GPT3.5-turbo and produce an audio of the answare (p2a) and lastly, use the created audio and translate it to Italian (a2a it).




<details>

<summary>Glossary of abbreviations</summary>

## Inputs and Outputs

```
c  -> code     ex: sourcecode of a python program
p  -> prompt     ex: "how can I escape the matrix?" 
t  -> text       ex: .txt file of a motivation letter
s  -> subtitle   ex: .srt file of a movie subtitles
a  -> audio      ex: .mp3 file of a recorded conference 
                 I/O: {sk -> speaker, m <- microphone} 
```
</details>

### Current state of implemented functions

|    	      | prompt   	| text | subtitle	| audio |  code 	|
|-----------|-----------|------|----------|-------|---------|
| prompt  	| `p2p`	| `p2t` 	|  `ap2s` *	| `p2a` | `p2c` 	|
| text  	  | t2p	| `t2t` | `at2s` * | `t2a` 	| `p2c` | 
| subtitle 	| - | `s2t`	| `s2s`	| `s2a`	| -	|
| audio   	|  `a2p` | `a2t`  | `a2s`	| `a2a` | a2c |
| code 	    |  - | - | - | - |  `c2c` 	|


## Features:

 * **Runs on Windows, Mac & Linux thanks to Docker**
 * Brings to your CLI only the best of the best of the latest AI technologies.
 * Modern [Charm](https://charm.sh/ "Charm") themale **TUI interface** written in Go.
 * Included **Markdown reader** for optimal formatting.
 * Focused on CPU **performance** and **consumer laptop** smooth exeperience 
 * Centralized environment file ( **.env** ) to set all your parameters
 * Docker in Docker architecture allows for extreme flexibility
 * Documented (very soon)
<details>

<summary>Concise pipelines (inputs2output)</summary>
 
 🔹 Ask gpt and gtts answer to **speaker** (text2speaker) -> t2sk <br /> 
 🔹 Ask gpt and gtts answer to **audio** (text2audio) -> t2a  <br />
 🔹 Ask gpt and produce specifically **code** (code2text) -> c2t  <br />
 🔹 Take audio and produce text **transcript** (audio2text) -> a2t  <br />
 🔹 Take audio and produce **subtitles** transcript (audio2subtitles) -> a2s  <br />
 🔹 Prompt gpt and produce text (prompt2text) -> p2t  <br />
 🔹 Take text and translate into text (text2text) -> t2tr  <br />
 🔹 Take audio and **enhance quality** into audio (audio2audio) -> a2a  <br />
 🔹 Take audio & text transcript and produce subtitles (audio+text2subtitles) -> at2s  <br />



 
</details>

### Screenshots & Tutorial: [Wiki](https://github.com/GabrieleRisso/MatrixGPT/edit/main/wiki.md "MatrixGPT Wiki")

 <p align="left"> <a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FGabrieleRisso%2Faiyu&count_bg=%234D4244&title_bg=%23EA2424&icon_color=%233E3636&title=aiyu+&edge_flat=false"/></a> </p>

## Dependancies: 

Install [Docker](https://docs.docker.com/engine/install/ "Docker")

## In the terminal:

###### download directory and enter it:
```
git clone https://github.com/GabrieleRisso/MatrixGPT.git 
cd MatrixGPT/
```
###### edit the .env file. (only the top section, the rest work by default): 
```
nano .env
```
###### OPTIONAL edit the setup script (the setup is guided ):  
```
nano setup
```

###### use it like this
```
matrix
```


##### Dependencies

They are prompted if missing and a link to install them is provided. Functions mostly leverages Python libs installed via pip and pre-build Docker images. Memory usage statistics will be out soon.


##### Who's project is doing the AI heavy lifting? 

 * [shell-gpt](https://github.com/TheR1D/shell_gpt "text-to-text")
 * [gtts](https://gtts.readthedocs.io/en/latest/index.html "text-to-speach")
 * [aeneas](https://github.com/readbeyond/aeneas "subtitles")
 * [translate-shell](https://github.com/soimort/translate-shell "translate")
 * [whisper-c2translate](https://github.com/jordimas/whisper-ctranslate2 "audio-to-text")
 * [mtts](https://github.com/mozilla/TTS "text-to-vocie")
 * [rnnnoise](https://github.com/GregorR/rnnoise-models "noise filter")
 * [stable-diffusion](https://github.com/fboulnois/stable-diffusion-docker "image gen")


### Open for collaboartions; let's make **aiyu** awesome toghter
 
 * per-command tuning
 * wiki documentation 
 * suggestions are desired!



### Citation
If you utilize this reposistory please consider citing it with:

```
@misc{aiyu,
  author = {Gabriele Risso},
  title = {aiyu: core shell functions for advanced ai},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/gabrielerisso/aiyu}},
}
```

### Copyright

Copyright © 2023 Gabriele Risso. 


#### Contact for custom implementation: 
```
gabriele.risso@protonmail.ch
```
