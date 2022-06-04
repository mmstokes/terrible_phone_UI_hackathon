# DTMFSelector #

A silly widget for selecting your phone number using DTMF (Dual-Tone Multi-Frequency) signaling.
Press the home row keys A, S, D, F, J, K, L in combination to produce the two tones that indicate the number you want to input. Enjoy the familiar sounds of touch-tone dialing.

Made for Tyler Maran @rysolv's May 2022 Terrible Phone Number UI Hackathon.

## Nerdy stuff: ##

In DTMF signaling (also known though the AT&T trademark "Touch-Tone"), the receiver can perceive the combination of two sine tone frequencies to indicate a particular key, where the key is the digit 0-9, star (*), or octothorpe/pound (#). Beyond these keys, A, B, C, and D are also included for special system codes through the use of an additional frequency, but they are not included in the DTMF Selector widget.

To keep with the spirit of how DTMF signaling works, I allowed my widget to "detect" the active frequencies. Each selected frequency was assigned a unique prime factor, and when that frequency is selected, the widget includes that factor with the other currently selected prime factors by multiplying them all together. The product of these factors is a unique representation of the currently selected frequencies. I mapped these unique products to the output signals 0-9, *, and #. In that way, the widget "detects" the combination of frequencies.
