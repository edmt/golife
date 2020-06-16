# Golife - A Game of Life project

[![Go Report Card](https://goreportcard.com/badge/github.com/ayoisaiah/golife)](https://goreportcard.com/report/github.com/ayoisaiah/golife)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/7136493cf477467387381890cb25dc9e)](https://www.codacy.com/manual/ayoisaiah/golife?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=ayoisaiah/golife&amp;utm_campaign=Badge_Grade)
[![HitCount](http://hits.dwyl.com/ayoisaiah/golife.svg)](http://hits.dwyl.com/ayoisaiah/golife)
[![PR's Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)

Simulate John Conway's Game of Life in your terminal. TUI is powered by [tcell](https://github.com/gdamore/tcell).

**Note**: This project was made as part of the [Project52 challenge](https://github.com/ayoisaiah/project52) in order to improve my Go skills.

## Installation

Make sure you have Go installed, then run the following command:

```
$ go get github.com/ayoisaiah/golife/cmd/...
```

Alternatively, you can download precompiled binaries for Linux, Windows, and macOS [here](https://github.com/ayoisaiah/golife/releases) (only for amd64).

## Usage

Basic usage:

```bash
$ golife
```

[See demo](https://asciinema.org/a/vklDi5cbwJYaEwXbrO2NORpqD)

### Preset patterns

Load preset from file ([example](https://gist.github.com/ayoisaiah/dedd29b0f02e7147c4832253c896ac88)):

```bash
$ golife --file gosperglidergun.cells
```

[See demo](https://asciinema.org/a/sMM4BBpt3sgjHcjvwrz8SBysY)

Load preset from URL ([see here](http://copy.sh/life/examples/)):

```bash
$ golife --url "http://copy.sh/life/examples/spider.rle" --input-format rle
```

[See demo](https://asciinema.org/a/EuNYaZssuCt00kYsD2GyU1J6L)

### Rules

The default rules are as follows:

- Any live cell with two or three live neighbours survives.
- Any dead cell with three live neighbours becomes a live cell.
- All other live cells die in the next generation. Similarly, all other dead cells stay dead.

However, there are other available rules. You can list them all using the following command:

```bash
$ golife rules
Default:
Survives: [2 3], Born: [3]

DayAndNight:
Survives: [3 5 6 7 8], Born: [3 6 7 8]

Coral:
Survives: [4 5 6 7 8], Born: [3]

2x2:
Survives: [1 2 5], Born: [3 6]

34Life:
Survives: [3 4], Born: [3 4]

Amoeba:
Survives: [1 3 5 8], Born: [3 5 7]

Assimilation:
Survives: [4 5 6 7], Born: [3 4 5]
...
```

Select a rule:

```bash
$ golife --rule WalledCities
```

[See demo](https://asciinema.org/a/ymVBKV06HwzqNjKbqIK1daurI)

### Themes

List available themes:

```bash
$ golife themes
WhiteOnBlack
BlackOnWhite
```

Select a theme:

```bash
$ golife --theme BlackOnWhite
```

[See demo](https://asciinema.org/a/qSIdcaCUkxIi8EKyHcg8wnSBH)

### Help

```bash
$ golife --help
```

## Credits

Golife relies heavily on other open source software listed below:

- [urfave/cli](https://github.com/urfave/cli)
- [gdamore/tcell](https://github.com/gdamore/tcell)
- [ayoisaiah/life](https://github.com/ayoisaiah/life)

## Contribute

Bug reports, or pull requests are much welcome!

## Licence

Created by Ayooluwa Isaiah and released under the terms of the [MIT Licence](http://opensource.org/licenses/MIT).
