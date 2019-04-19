# unicode-chars-database

I presumed it would be easy to find something like a C header file full of `#define`s linking literal names to codes of Unicode characters.

It wasn't. (April 2019 then.)

Maybe a simple table, a CSV file. Okay if only the Basic Multilingual Plane, all you can eat with 16 bit(e)s. There were a lot of wonderful reference sites, but I could not find something I could use for showing characters and their names in a simple desktop app.

It seems almost certain that some clever people found clever solutions for such task if they ever needed or wanted it, but I am just naïve and fool, so I thought that an open, shared collection of data about Unicode characters might be useful or simply interesting for somebody (else than me).

## Goals

- To create a list of basic data about the Unicode characters, at least the 65.536 initial codepoints.

- Such list should be simultaneously (automatically, who knows) maintained in various machine-friendly formats. A CSV table is the primary goal, a C/C++ `#include` header file immediately following, and if anybody would like to create an equivalent file or database for their preferred language, format or application it would be happily incorporated.

- To collect public, open information (data or code) about the subject. 

## Data about characters

I think the following data about each character would make for a useful table:

- Official Unicode name
- Codepoint
- UTF-8 encoding
- UCS-2 encoding
- UTF-16 encoding
- Alt code (used to type the character)
- HTML encoding entity
- Unicode set
- Script
- Unicode plane


## Links
