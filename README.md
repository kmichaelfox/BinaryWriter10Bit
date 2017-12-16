# BinaryWriter10Bit

This plugin is a recording engine for Open-Ephys that writes interleaved bytes packed with 10-bit samples.

Samples are converted to 16-bit little-endian integers that discard the 6 least significant bits. Samples then are packed into overlapping bytes so that there is no padding between values---eight 10-bit samples are distributed over five 16-bit addresses.

After packing, the channel data is interleaved *by byte*, instead of *by sample*, and written to file.
