<p align="center">
    <img src="./resources/logo.png" width="500px">
</p>

<h1 align="center"><p align="center">CAH Generator</h1></h1>

> Created by **Miguel Ángel Fernández Gutiérrez** · https://mianfg.bloomgogo.com/

## Introduction

**CAH Generator** is a card generator for the game [_Cards Against Humanity_](https://cardsagainsthumanity.com/), a party game for horrible people.

This generator enables you to:
* Generate cards using various formats and styles (more information below).
* Include your own CAH game. For example, if your game is a CAH fork called ***Ysabel Against Humanity***, you can have your own watermark!
* Include game version.
* Automatic PICK and DRAW for black cards.
* Special cards.

## Use

You need to have **Ruby** installed, at least 2.5. Then you can, from your console:

```
ruby generator.rb
```

By default, a help message will be displayed. Follow the instructions for more.

## Generator features

The generator works using three files:
* `white.txt`, the white cards file.
* `black.txt`, the black cards file.
* `info.txt`, the game info file, where you can specify the name of your game and, optionally, the game version.

### Info file

If the info file is available, the generator will introduce your game name in every card. Refer to the help text for more information on this file's format.

### White and black cards

Each card must be in one line. Zero-length lines will be ignored, but lines containing spaces will be turned into blank cards.

Inserting `((_))` on any line will generate a special card, that has as icon the character `_` (i.e., for _warning_ cards, put `((!))`).

The generator has **PICK 2 and PICK 3 detection**, but you can manually insert them by adding `[[2]]` or `[[3]]` at the beggining or the end of the line.

Card text can be **formatted** using HTML-like tags. The supported tags are:

- `<b></b>` - bold text
- `<i></i>` - italic text
- `<u></u>` - underlined text
- `<strikethrough></strikethrough>` - strikethrough text
- `<sub></sub>` - subscript text
- `<sup></sup>` - superscript text
- `<br>` - line break
- `<color rgb=\"#0000ff\"></color>` - set text color
- `<font name=\"Font Name\"></font>` - set text font

### Card sizes

You can specify different card sizes:

* **Large:** cards of size 2.5" x 3.5"
* **Small:** cards of size 2" x 2"

## Credits

This project is a fork of [Bigger, Blacker Cards](https://github.com/bbcards/bbcards).

## Disclaimer

This site is not affiliated with nor endorsed by Cards Against Humanity, LLC. Cards Against Humanity is a trademark of Cards Against Humanity LLC. Cards Against Humanity is distributed under a Creative Commons BY-NC-SA 2.0 license - that means you can freely use and modify the game but aren't allowed to make money from it without the permission of Cards Against Humanity LLC.

Don't use this tool to infringe anyone's intellectual property. Do NOT just plug in the text for existing non-public card packs, that Cards Against Humanity, LLC is selling. That's just not cool. Instead, go to http://www.cardsagainsthumanity.com, and buy their stuff. They made an awesome game, they deserve your money. This tool is for making your own cards, not theirs. That's why there's an option to make big 2.5"x3.5" cards -- that way you can print your own custom cards that are the same size as the official, purchased cards, so they can be used together.
