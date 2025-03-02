# German Word Clock Face Documentation

## Overview
The German word clock face displays time in a natural language format using an 11x11 LED matrix. It supports both standard German time format ("DREIVIERTEL VIER") and regional variations like ("VIERTEL VOR VIER").

## LED Layout

### LED Matrix (IDs)
```
|110|111|112|113|114|115|116|117|118|119|120|
|109|108|107|106|105|104|103|102|101|100| 99|
| 88| 89| 90| 91| 92| 93| 94| 95| 96| 97| 98|
| 87| 86| 85| 84| 83| 82| 81| 80| 79| 78| 77|
| 66| 67| 68| 69| 70| 71| 72| 73| 74| 75| 76|
| 65| 64| 63| 62| 61| 60| 59| 58| 57| 56| 55|
| 44| 45| 46| 47| 48| 49| 50| 51| 52| 53| 54|
| 43| 42| 41| 40| 39| 38| 37| 36| 35| 34| 33|
| 22| 23| 24| 25| 26| 27| 28| 29| 30| 31| 32|
| 21| 20| 19| 18| 17| 16| 15| 14| 13| 12| 11|
| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |10 |
```

### Letter Matrix
```
| E | S | K | I | S | T | L | F | Ü | N | F |
| Z | E | H | N | Z | W | A | N | Z | I | G |
| D | R | E | I | V | I | E | R | T | E | L |
| T | G | N | A | C | H | V | O | R | J | M |
| H | A | L | B | X | Z | W | Ö | L | F | P |
| Z | W | E | I | N | S | I | E | B | E | N |
| K | D | R | E | I | R | H | F | Ü | N | F |
| E | L | F | N | E | U | N | V | I | E | R |
| W | A | C | H | T | Z | E | H | N | R | S |
| B | S | E | C | H | S | F | M | U | H | R |
| E | V | ° | X | ° | N | ° | S | ° | P | I |
```

## Time Format Examples

### Standard German Format
- 3:00 - "ES IST DREI UHR"
- 3:05 - "ES IST FÜNF NACH DREI"
- 3:10 - "ES IST ZEHN NACH DREI"
- 3:15 - "ES IST VIERTEL VIER"
- 3:20 - "ES IST ZWANZIG NACH DREI"
- 3:25 - "ES IST FÜNF VOR HALB VIER"
- 3:30 - "ES IST HALB VIER"
- 3:35 - "ES IST FÜNF NACH HALB VIER"
- 3:40 - "ES IST ZWANZIG VOR VIER"
- 3:45 - "ES IST DREIVIERTEL VIER"
- 3:50 - "ES IST ZEHN VOR VIER"
- 3:55 - "ES IST FÜNF VOR VIER"

### Regional Format
- 3:15 - "ES IST VIERTEL NACH DREI"
- 3:45 - "ES IST VIERTEL VOR VIER"

## Special Features
- Minute dots (°) can be used as status indicators

## Implementation Notes
- LED numbering starts from bottom left (0) to top right (120), like a snake
- LED ranges are defined as pairs of (startIndex, length)
- The format can be switched between standard and regional through configuration