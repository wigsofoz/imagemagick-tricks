# Box around image with drop shadow

    convert SourceFile.png -bordercolor black -border 1 \
        \( +clone -background black -shadow 80x3+2+2 \) +swap \
        -background matte -layers merge +repage \
        OutputFile.png

