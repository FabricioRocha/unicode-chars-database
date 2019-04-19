# unicode-chars-database

I presumed it would be easy to find something like a single table or a C header file full of `#define`'s linking literal names to codes of Unicode characters.

It wasn't. (April 2019 then.)

So I naïvely decided to create one. 

It seems almost certain that some clever people found clever solutions for such task if they ever needed or wanted it, and maybe there's more people who would have a use or simple interest on something like that, so I thought it would be nice to put it here.

## Goals

- To create a list of basic data about the Unicode characters, at least the 65.536 initial codepoints of the Basic Multilingual Plane (as it's all you can eat with 16 bit(e)s).

- Such list should be simultaneously (automatically, who knows) maintained in various machine-friendly formats. A CSV table is the primary goal, a C/C++ `#include` header file immediately following, and if anybody would like to create an equivalent file or database for their preferred language, format or application it would be happily incorporated.

- To collect public, open information (data or code) about the subject. 

## Data about characters

I think the following data about each character would make for a useful table:

- **Codepoint** - in C hexadecimal notation (0x...)
- **Name** - official Unicode name
- **UTF-8** - 8-bits multibyte encoding with no zeores
- **UCS-2** - the "wide char" encoding
- **UTF-16** - 16-bit multibyte encoding, little-endian (Intel) order
- **AltCode** - what code to type while pressing Alt in order to get the character from a keyboard
- **HTML** - the code to show the character in HTML
- **UnicodeSet** - name of the Unicode set the character belongs to
- **UnicodeBlock** - name of the Unicode block (seems somewhat related to scripts)
- **UnicodePlane** - name of the Unicode plane the character belongs to
- **UnicodeScript** - the "alphabet" which uses this character, according to Unicode (roughly speaking, I know)


## Links

[GNU libunistring](https://www.gnu.org/software/libunistring/) - a C library which gives you that (in runtime). I haven't used it yet. It seems to generate the names from a specially formatted [table of codes](https://fossies.org/linux/libunistring/lib/uniname/uninames.h).