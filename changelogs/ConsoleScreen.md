# Console Screen Change Log
All notable changes to this project will be documented in this file.

## 1.5.0 - 2016-06-27
### Added
- Cursor switches. Cursor no longer must affect the its cell's colours and it can invert its cell's colours
- Ignored cursor value. A cursor value that is negative values will not affect its cell's value
- A mapped character can be used to set the cursor's value

### Changed
- Class name is now ConsoleScreenV1 and the filenames now have been appended with "Old" in preparation for the additional inclusion of version 2.

### Fixed
- Cursor now never stretches regardless of the cell's stretch value.

## [1.4.0] - 2016-03-29
### Added
- Character mapping. Printed characters can now be mapped to any cell value
- Reading. Retrieves a string from consecutive cells. Can use cursor or read directly
- Texture offset. A sub-texture can now be used

### Fixed
- Colour commands now processed for every cell individually in paintAt()

## [1.3.1] - 2016-03-28
### Fixed
- Colour commands now functions correctly when using printStretchedAt() ([#5])

## [1.3.0] - 2016-03-11
### Added
- Double-height printing. Each half can be printed separately or together
- Cell attributes:
    - Inverse swaps colour and background colour
    - Bright displays fully bright colour (darkens when switched off)
    - FlipX and FlipY flip the cell horizontally and vertically respectively

## [1.2.1] - 2016-02-09
### Fixed
- Buffer width now correctly calculated when selection rectangle extends beyond screen limits ([#3])

## [1.2.0] - 2016-02-07
### Added
- Buffers/clipboards (entire screen or rectangular regions)
- Painting: similar to printing but doesn't affect cell values (only alters colours), like highlighting
- Cell information retrieval to allow getting a cell's value, colour, background colour, or entire cell

### Removed
- "Greyscale" from palette enum. Now only "grayscale" can be used

## [1.1.0] - 2016-01-12
### Added
- Colour palettes
- Colour commands
- Customisable cursor
- Text-editing cursor controls

### Changed
- printAt() now prints both string and characters so printCharAt() has been removed
- Nullifying the texture no longer requires (or accepts) a null pointer to be passed as a parameter
- All switch/flag methods have had "enabled" removed from their name
Some renamed slightly for grammatical reasons
- nextline() has been renamed as cursorNextline() to increase naming consistency

## [1.0.0] - 2016-01-02
### Added
- Full version

[1.4.0]: https://github.com/Hapaxia/SelbaWard/commit/3dc18730df9a096d5bbf80d19e7e839357fc985d
[1.3.1]: https://github.com/Hapaxia/SelbaWard/commit/f544eaf2e90d46558dcaeb80c54992def0a18ec8
[1.3.0]: https://github.com/Hapaxia/SelbaWard/commit/661223c925e9c1d57ce11f77462812cd024f9aa9
[1.2.1]: https://github.com/Hapaxia/SelbaWard/commit/2238bc8dfec3580d7da7188bf9a388b5e720ca2e
[1.2.0]: https://github.com/Hapaxia/SelbaWard/commit/37a22dbf625ce1468077c2455266a4b41651952d
[1.1.0]: https://github.com/Hapaxia/SelbaWard/commit/869078f4294e62814c43d63416b5a68af9c5363d
[1.0.0]: https://github.com/Hapaxia/SelbaWard/commit/424ca290165d74de99d00806166dc0b52eb6d5f0

[#3]: https://github.com/Hapaxia/SelbaWard/pull/3
[#5]: https://github.com/Hapaxia/SelbaWard/pull/5