# claude-edits

The photo and video edits from the AI Owl reels ([@owlexplainsai](https://www.instagram.com/owlexplainsai)), with the exact prompts. Copy a prompt, attach your own photo or clips, and change the words in it to fit your shot.

Made with Claude Opus 5.5. Free, MIT licence.

## 1. A horizontal photo, made vertical without cropping

```
Make this vertical for a reel. Don't crop anything. Extend the sky and the river.
```

**Needs:** the Adobe connector in Claude. Attach the photo with the prompt.

**What happens:** Claude sends the photo to Photoshop's Generative Expand and brings back a 9:16 version. Your original pixels stay as they were; only the sky and river around them are generated. Change "the sky and the river" to whatever is above and below your subject.

## 2. Five photo edits, one line each

| # | Edit | Prompt | Needs |
|---|---|---|---|
| 01 | Text behind the mountain | `Write SUKOON behind the mountain` | Adobe connector (Photoshop's select-by-prompt finds the sky), and Claude running code to place the word between the sky and the ridge |
| 02 | Colour pop | `Keep only her in colour` | Adobe connector (select the person by prompt, invert, remove the colour from the rest) |
| 03 | Horizontal to vertical | `Make it vertical. Don't crop.` | Adobe connector (Generative Expand) |
| 04 | 3D photo | `Make this photo move in 3D` | Claude running code: a free Hugging Face model, Depth Anything V2, makes a depth map, and a short script moves a camera through it |
| 05 | Zoom out | `Zoom out. Show me more.` | Adobe connector (Generative Expand, twice, then one continuous zoom) |

Swap SUKOON, "her" and "the mountain" for your own word, person and background.

## 3. A velocity edit, on the beat

```
Here are my raw drone clips and a song. Find the beat, pick the best moments, and cut a reel where every cut lands on the beat. Start each shot in slow motion and speed it up into the next cut. Go slow motion where the beat stops.
```

**Needs:** Claude running code on your files (for example Claude Code, or the Claude desktop app with the folder connected). Put the clips and the song in one folder. Claude uses Python with ffmpeg and OpenCV and installs what's missing.

**Tips:**
- 60 fps footage gives real slow motion at half speed.
- If the cuts feel off the beat, ask Claude to find the tempo from the kick drum. Songs with a 3+3+2 rhythm (a lot of Bollywood, reggaeton and afrobeats) fool a standard beat tracker: in the reel, one said 136 BPM for a 102 BPM song.
- Ask for the shots where the camera actually moves. A speed ramp on a hovering drone still looks static.

## 4. A grid edit, on the beat

```
Here are my raw drone clips and a song. Find the beat and pick the best shots. Cut a grid edit: open on a 3x3 of shots, then splits, 2x2 and columns, a new layout every bar and every cut on the beat. End on the best shot, full screen.
```

**Needs:** the same as 3.

## Music

Use songs you have the rights to use.

## About

By Rohan J: [@owlexplainsai](https://www.instagram.com/owlexplainsai) on Instagram, [@rohanbuilds-ai](https://www.youtube.com/@rohanbuilds-ai) on YouTube.
