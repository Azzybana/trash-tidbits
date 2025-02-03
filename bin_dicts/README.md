# Binary Dicts

## About

Starting to work on my own take on a language model. After reading about how they work, I think I have a better way to do it. For pre-training, going to need to know character weights. To speed that up, I want to selectively choose what to enumerate. I want it to forget the symbols it doesn't need, and learn new ones it does.

Noise reduction has maths. For starting points, I've created a couple of dicts. Nothing special about them, use them or not, WTFPLv2 from my end on the dicts, since it's literally just byte-dumped utf32-le character ranges. Everything aligned to 32bits, so easy to read back in.

## License

WTFPLv2 on this folder, since it's just UTF32-LE dumps. I mean, acknowledge would be nice, lol.

## Contents

safe_dictionary.bin is 587kb, includes every range defined that I could find, anywhere. Except the undefined PUA ranges.

asian_dictionary.bin is 483kb, all 5 major Asian groups, and nothing else.

lean_dictionary.bin is 105kb, and includes every known symbol besides the 5 major Asian groups

tiny_dictionary.bin is 17kb, covers all of the Latin pages, numerical, scientific, emoji, corporate, etc. No Cyrillic or Greek or Arabic, etc.
