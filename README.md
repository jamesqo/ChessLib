# ChessLib
A C# chess data library with complete move generation and all needed custom types.

[![Build status](https://ci.appveyor.com/api/projects/status/6dksl8dsq5s1n2uv/branch/master?svg=true)](https://ci.appveyor.com/project/rudzen/chesslib/branch/master)

## Requirements

ChessLib is using NET_STANDARD 2.0, which enables it to be used with the follow

* .NET Framework 4.6.1+
* .NET Core 2.0+
* Mono 5.4+
* Xamarin.iOS 10.14+
* Xamarin.Mac 3.8+
* Xamarin.Android 7.5+

## What is this for?

This library contains all the data, types and structures for which to create a piece of
chess software. It does not contain any heuristics or search algorithms as these
are ment to be implemented separatly.

## But why?

This library was developed during a course "Advanced C# and object oriented programming E17" at DTU (Danish Technical University) as part of a chess user interface, which will be released at a later stage when it is ready.
Since the UI needs to handle legality, mate check etc etc, all these features are contained within the library.

## Can i use this as a starting point for my chess software?

Yes you can, it is designed with that in mind.

## Features

* Complete move generation with legality check.
* Custom compact and very efficient types for Bitboard, Square, Piece, Move, Player, File, Rank and Direction with tons of operators and helper functionality.
* 100% Bitboard support with piece attacks for all types, including lots of helper functions.
* Lots of pre-calculated bitboard arrays to aid in the creation of an evaluation functionality.
* FEN handling with optional legality check.
* Magic bitboard implementation Copyright (C) 2007 Pradyumna Kannan. Converted to C#.
* FEN input and output supported.
* Chess960 support.
* Zobrist key support.
* Basic UCI structure.
* HiRes timer.
* Draw by repetition detection.
* Mate validation.
* Plenty of unit tests to see how it works.
* Notation generation for the following notation types: Fan, San, Lan, Ran, Uci.
* Basic perft project included, performs depth 6 (119060324 moves) on a AMD-FX 8350 in ~12.5 seconds.
* Benchmark project for perft.

## Is it fast?

Yes. As far as C# goes it should be able to hold its own.

Perft console test program approximate timings to depth 6

* AMD-FX 8350 = ~12.5 seconds.
* Intel i7-8086k = ~6.2 seconds.

## What is not included?

* Evaluation
* Search
* Transposition table
* Communication using e.i. UCI (base parameter struct supplied though)

## Planned

* Transposition table
* Better move generation with staged enumerator
* Better state structure
