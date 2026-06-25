# musicxmlTestSuite

MusicXML Test Suite (Unofficial)

This is a fork of Reinhold Kainhofer's extensive MusicXML test suite 
developed for testing Lilypond's `musicxml2ly` program.  Since it is
useful for lots of music projects that want to support MusicXML
(such as the `music21` project), I've forked it here with Reinhold 
Kainhofer's blessing and invite contributions of new tests for the future.

# Usage

The test suite borrows the structure of the original Lilypond test suite, with some changes.

* 01-03: Basics: Pitches, Rests, Rhythm
* 11-14: Staff attributes: Time, Clefs, Key
* 21-24: Notes, Chords, Tuplets, Grace
* 31-34: Notations and articulations
* 41-43: Parts
* 45-46: Repeats, Barlines, Measures
* 51-52: Page layout
* 55-59: Other positioning and layout
* 61: Lyrics
* 71-75: Instrument-specific
* 81-89: MIDI and Sound
* 90: Compressed MusicXML and other MusicXML Formats
* 95-99: Ambiguities, Issues, and Problems
  - 95: Interpretation of changed specifications in different MusicXML versions (unused)
  - 96: Ambiguous situations (unused)
  - 97: Contradictory MusicXML instructions (3/4 + cut time, etc.) (unused)
  - 98: Compatibility with nonsensical but in spec. MusicXML (unused)
  - 99: Compatibility with broken MusicXML (against spec. etc.) found in exports


## Significant changes from the Lilypond test suite:

* Tests have been broken up so that initial tests cover only the most common uses of a particular tag or attribute (such as key signatures from 7 flats to 7 sharps) and later tests cover valid but unusual usages (keys of 11 sharps, mid-measure key changes, etc.)
* Against spec examples that would break an XML validator are all collected under category 99. (For instance, incorrect accordion registration was moved to 99d from 75a.)  Note that 99c is not technically broken musicxml -- it should be in 98.

# Copyright and License

Originally Copyright (c) 2010–2016, Reinhold Kainhofer and the GNU Lilypond
project.  The MusicXML files in that suite and edited here have been released
under the MIT License, see LICENSE for more details.
Free for any use as long as this license remains intact.

Developed 2016–2026 by Michael Scott Asato Cuthbert
