# Capture waveform

Use Audigy

# Encoding Type

manchester - https://en.wikipedia.org/wiki/Manchester_code
None-return-to-zero - https://en.wikipedia.org/wiki/Non-return-to-zero
based on width of pulses 

# Layout

* device id
* checksum
* payload

# checksum

Simple addition + constant - Nope

Simple XOR + constanct- Nope

Try CRCs - no luck
  - make sure to try different bit orders (LSB, MSB etc.)
  https://sourceforge.net/projects/reveng/files/

Simple addition 4 bit nibles
 - bottom yes
 - top no

4 bit Fletcher ? - uses 2 4 bit sums
 - no, tried all byte orders

49 fd 00 4c
4f e3 00 4c
CF e2 00 4c
CA F6 00 34
D0 FC 00 34
51 FD 00 34
52 FE 00 34
D3 FF 00 34
98 03 01 34
