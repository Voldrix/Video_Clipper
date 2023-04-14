# Video Clipper

### _quickly clip segments of a video, and generate FFmpeg code to concatenate into single highlight reel_

A single page, in-browser, video cropper. Cut a sequence of clips and concatenate them into a highlight reel.\
The page cannot render the video directly, instead it generates the FFmpeg command with the appropriate clip timings.

### Usage
Open the static HTML file in your browser, load a video, make a series of clips, then hit render to generate the code. Copy that code into a bash shell on Linux. FFmpeg is required.

There are two scrub bars, the top one is the duration of the video. The bottom one is for precision, it only extends two seconds in either direction from the position of the top scrub bar.

The clips can be reordered by dragging them.

To start a new video, drag and drop it over top the current video. This will clear all current clips, as multiple source videos is not yet supported.

### Keyboard Shortcuts
- `Space` play / pause
- `I` set clip IN point
- `O` set clip OUT point
- `C` Clip. Add clip to list, from current in point to current out point
- `R` Render FFmpeg code to generate highlight reel
- `Right Arrow` Seek +10s
- `Left Arrow` Seek -10s
- `]` Seek +1s
- `[` Seek -1s
- `>` Seek +1 frame
- `<` Seek -1 frame
- `;` Seek to IN point
- `'` Seek to OUT point

__Limitations__\
not designed to work on mobile.\
media codec support is dependent on your browser.

### Contributing
UI / design improvements are welcome if you have a good eye for clean / minimal design.

__TODO__
- scrub bar progress meter missing in WebKit
- scrub bar thumb incorrect in WebKit
- enable clips from multiple source videos

__License__\
[MIT License](!LICENSE)

