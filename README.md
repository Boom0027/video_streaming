# Ways of video playback in html

## Video with a source - Plays the first recognized source
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>

## MSE - Media source extensions
1. Instead of adding a source, we can use AJAX to request for requesting chunks and play the video accordingly

## DASH or MPEG-DASH - Dynamic adaptive streaming over http
1. Deliver video to the user in the most efficient way possible
2. Should be in the highest usable quality for each specific user
3. We have different quality video and audio file and switch according to the bandwidth of the user
4. This is in combination with MSE. Fill the buffer with lower or higher quality video depending on the bandwidth
5. We create a manifest and hand it over to any dash compatible video player and it is able to play the video accordingly.
6. The manifest contains the list of files qualities, codec and the bandwidth required to play them.

## HLS - Http live streaming
1. Dash might not be compatible to some devices, so we can use HLS. 
2. Similar to dash
3. Creates an HLS manifest, m3u8 manifest.
4. In mobile we give the m3u8 file as the video source and it will do the rest