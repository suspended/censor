# censor
Suppress unacceptable parts of audio and video

This is a proof of concept and specification for suppressing parts of a video.

For example while watching a movie this technique will automatically mute profanity and skip nudity.

This technique works similar to subtitles where there is a file with instructions which the video player will load and follow.

So basically for version 1 below are the specifications

1. Filename should be same as video name with .censor extension.
2. A number indicating which censor it is in the sequence.
3. Same line can optionally add comment starting with #
2. The time that the censor should activate, and then diactivate.
3. Instruction (MUTE,SKIP)
4. A blank line indicating the start of a new censor.

Example:
```
1 #this scene there is foul langauge
00:02:17,440 -- 00:02:20,375
MUTE

2 #this scene contains violence
00:02:20,476 -- 00:02:22,501
SKIP
```
