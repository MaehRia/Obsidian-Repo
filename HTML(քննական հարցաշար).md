
# 1. Տառատեսակների տեսակները, հիմնական հատկությունները։

Տառատեսակների հիմնական ընտանիքներն են։

1. Serif (Times New Roman, Georgia)
2. Sans-Serif (Arial, Helvetica, Verdana)
3. Monospace (Monaco, Consolas)
4. Cursive (Comic Sans MS)
5. Fantasy (Papyrus)

Main properties in CSS:

Examples.

`font-family: Arial;
`font-size: 20px;
`font-weight: normal/lighter, bold, 900;
`font-style: normal, italic, oblique;
`letter-spacing: px;
`line-height: px;

# 2. Եզրագծեր, եզրագծերի ոճավորումը և ներկայացման ձևերը։

Եզրագծերի հիմնական հատկությունները CSS-ում․

Եզրագիծը (border) ունի մի քանի հիմնական հատկություն՝

- **`border-width`** – սահմանում է եզրագծի հաստությունը։
- **`border-style`** – սահմանում է եզրագծի ոճը։
- **`border-color`** – սահմանում է եզրագծի գույնը։

![[Pasted image 20250120022630.png|500]] 
Եզրագծերի կողմերի առանձին ձևավորում։

```css
div {
  border-top: 2px solid black;
  border-right: 3px dotted green;
  border-bottom: 4px dashed red;
  border-left: 1px double blue;
}
```