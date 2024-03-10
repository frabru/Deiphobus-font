# Deiphobus typeface design guide


## Design space

![Design space](./graphics/design_space.svg)

The glyphs are mostly designed in a 96×128 (32·3×4) rectangle, the wider letters 'M' and 'W' in a 128×128 (32·4×4) square. From that design space they are scaled up by a factor of 11, chosen so that the cap height is close to 70% of the standard em-size of 2048.

The glyphs are given 16 units in design space (16·11 = 176 units in font coordinates) of padding on both the left and the right side, so that when no kerning rules apply, the spacing between adjacent letters will be 32 design space units (352 font coordinate units).


## Glyph geometry

![Glyph geometry](./graphics/glyph_geometry.svg)

The regular glyph stem width is 34 (374 in font coordinates). This value is chosen because it gives us 48 as a good approximation of √2 times the stem width and 38 as a good approximation of ½·√5 times the stem width, which are needed to get about the same width for 1:1 (45°) and 2:1 slopes, respectively.

Only straight line segments are used; and mostly only lines that are horizontal, vertical, at 1:1 (45°) slopes or 1:2 or 2:1 slopes. Other angles are only used in the asterisk glyph, because all draft designs of asterisks within the usual design rules were deemed unsatisfactory.

Where the general glyph shape would have curved lines, in this typeface the inner curve is represented by rectangular or triangular shapes, whereas the outer curve's representation changes angles in 45° increments, forming octagonal shapes. All lines of the outer curve are generally at a distance of about 34 units from the corners of the inner shape. For horizontal and vertical lines that means exactly 34 units distance. The diagonal lines are closest to the inner corner points at an offet of (24; 24) which is at a distance of 24·√2 ≈ 33.9411 . The letter ‹B› deviates from these metrics, because strict adherence to these distances would leave the indent where both arcs meet unnoticeably small.

Diacritics are designed with a smaller stem width of 24 and use 34 as their approximation of √2 times the stem width.

Shortened variants of base glyphs (with the name suffix «.short») for use with diacritics have their height reduced by 14 units, reducing them to 114 units.


## Glyph design

Despite the blocky geometric style of the typeface, glyphs are designed to be distinguishable even where the generic shapes of letters are similar. The design takes direct inspiration from the forgery-impeding typefaces used on vehicle registration plates.

![Forgery-impeding design](./graphics/impeding_forgery.svg)

The glyphs are primarily sans-serifs. But the Latin letter ‹I› has slab serifs to make it occupy the same width as the majority of the letters. Its upper serifs are shorter than the lower ones to distinguish it from ‹T› even when the bottom is obscured. The Latin letter ‹J› has a slab serif to distinguish it from ‹U› even when the left side is obscured. Latin letter ‹L› has a slab serif to distinguish it from ‹E›. Greek letter ‹Γ› has a slab serif to distinguish it from ‹Π› even when the right side is obscured. Cyrillic letter ‹Г› has slab serifs to distinguish it from ‹П› and ‹Б›. And the digit ‹1› has an underline/slab serifs to make it clearly distinct from a ‹7› even when the text orientation is unclear and the reader is unfamiliar with the typeface's digit designs.

Some characters with diacritical marks above use a shortened form of the base character so that it would be noticeable if diacritical marks were just drawn onto the regular base character. This was added in version 1.3 and isn't implemented for all characters yet. The main goal was to distinguish umlauts for German. Cyrillic ‹Й› and ‹Ѝ› instead use a base character of the same height as ‹И› but with the diagonal stroke placed lower.

Characters of different scripts that share the same basic shape only reuse the same glyph outline if they generally have equal or near equal sound value and are transcibed as each other.

* Thus Latin ‹A›, Greek ‹Α›, and Cyrillic ‹А› have the same outline.
* But Cyrillic ‹В› has a design distinct from Latin ‹B›. The Cyrillic letter is symmetric in analogy to a sideways turned ‹W›, because ‹W› would be the Polish equivalent to Cyrillic ‹В›. And Greek ‹Β› has yet another redesign, because while it is transcribed as and historically pronounced like Latin ‹B›, its pronunciation in modern Greek is like Cyrillic ‹В›. So neither of them is an acceptable equivalent.
* The horizontal stroke in Greek ‹Η› is higher than in the symmetrical Latin ‹H›, and in Cyrillic ‹Н› the horizontal stroke has a notch which also serves to impede changing ‹Ч› to ‹Н›.
* Greek ‹Ρ› and Cyrillic ‹Р› share the same outline, but Latin ‹P› differs from them, while the former two share the triangular arc with Latin ‹R›.
* Latin ‹Y›, being the Greek letter ‹Υ› imported into the Latin alphabet does share the same outline. Because of the different pronunciation and transcription it might get redesigned in a future version.
* Greek ‹Χ› and Cyrillic ‹Х› share the same outline, but Latin ‹X› differs from them.
* Cyrillic ‹С› has a small chip at the bottom edge of the top stroke that distinguishes it from Latin ‹C› but is shared with Latin ‹S›.
* Cyrillic ‹Ѕ› has bevelled stroke ends unlike Latin ‹S›

Other inter-script redesigns are motivated by the forgery-impeding goal.

* Latin ‹O› and Cyrillic ‹О› use the obvious outline based on the glyph geometry guide. By adding a horizontal stroke in the middle, this could be changed into a Greek ‹Θ›. Therefore the Greek ‹Ο› has a different top with a non-rectangular inner curve that would be very noticeable if split horizontally.
* Greek ‹Φ› has a very different outline from Cyrillic ‹Ф›, partly because Greek has the letter ‹Ψ› that could be altered.
* Cyrillic ‹М› uses the same angle and if the right half is obscured would look the same as Latin ‹N› and Greek ‹Ν›. Therefore Latin ‹M› and Greek ‹Μ› use a different outline with 45° angles.

Some inter-script redesigns are just aesthetic choices.

* Greek ‹Δ› and ‹Λ› have outlines that would be acceptable to reuse for Cyrillic ‹Д› and ‹Л›. But the Cyrillic letters were instead designed based on more uniquely Cyrillic variant shapes of these glyphs.
