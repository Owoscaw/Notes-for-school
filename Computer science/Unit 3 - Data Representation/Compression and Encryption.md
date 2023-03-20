
Data can be compressed in order to reduce its file size. There are two ways in which data can be compressed - lossy and lossless. In general, lossy compression can reduce file size to a greater degree than lossless compression.

## Lossy:

Non-essential data is removed permanently, this data is lost - however it is deemed inessential to represent the original piece of data. For example, frequencies above the range of human hearing and different shades of the same colour can be removed in order to reduce file size.

JPG image formats permanently reduces file size by discarding data, then tries to reconstruct an image without the data that was discarded.

MP3 [[Representation of Sound|sound formats]] remove the sounds in frequency ranges that cannot be perceived by humans. 

## Lossless:

Patterns are found in the data, which are then summarised in a shorter format without permanently removing any data. Text files, or any file formats conveying text, must be used with lossless compression. This is because the file can become illegable and all meaning is lost when data is removed.

## RLE:

Run Length Encoding is a basic method of lossless compression that summarises consecutive patterns in data. Instead of 10 consecutive blue pixels, "10" followed by a blue pixel can be recorded. This represents 10 times blue pixel, which is reconstructed to 10 consecutive blue pixels.

This can also be used in a sound recording by replacing the same sound or note in consecutive samples with the same representation as above.

## Dictionary compression:

Dictionary compression spots regularly occuring data and stores it in a seperate dictrionary. This is largely used in text file compression, as it is lossless. For example, in the phrase "no pain no gain", "no" can be replaced with a binary token, as well as "ain". This is also done for every character that is not part of an already represented series of characters.