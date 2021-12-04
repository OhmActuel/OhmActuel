👋 Hi, **I’m OhmActuel**

This account will host more interesting projects in the near (?) future.
On the meantime I'll use this readme as a notebook for useful info (mostly bash commands).

# Useful Bash commands

##### Recover a corrupted docx file:
    unzip -p some.docx word/document.xml | sed -e 's/<[^>]\{1,\}>//g; s/[^[:print:]]\{1,\}//g'

##### Embbed (hardsub) files to a video with ffmpeg:
    ffmpeg -i video.mp4 -filter:v subtitles=subtitles.srt -strict -2 video_with_subs.mp4

> Note : no "-strict -2" needed for avi videos

> Note : make sure that the subtitles are encoded in UTF-8. If not, they can be resaved in a new file

##### Convert videos:
    ffmpeg -i video.mp4 video.avi

##### Change filenames extensions:
    rename 's/\.old$/.new/' *.old

##### Resize images with imagemagick:
    magick mogrify -resize XX% <filepath>

> Note: "magick" is optional!
