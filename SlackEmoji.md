# Creating a Slack Emoji

Slack wants a 128x128 pixel image. Replacing any background border with a transparent matte makes the image look a bit more
consistent on different text backgrounds.

    convert -alpha set -channel alpha -fill none -fuzz 10% -floodfill +0+0 white -trim \
        -resize 128x ORIGINALFILENAME EMOJINAME.png

