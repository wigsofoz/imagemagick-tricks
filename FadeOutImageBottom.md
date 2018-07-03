# Fade out image bottom

    identify OriginalFile.png
    
    convert -size ${WIDTH}x${HEIGHT-GRADIENTWIDTH} xc:white \
        -size ${WIDTH}x${GRADIENTWIDTH} gradient: \
        -append TemporaryMask.png
    
    convert OriginalFile.png -compose copy_opacity TemporaryMask.png \
         -gravity South -composite \
         OutputFile.png

