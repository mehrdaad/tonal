# tonal-pitch [![npm version](https://img.shields.io/npm/v/tonal-pitch.svg)](https://www.npmjs.com/package/tonal-pitch)

[![tonal](https://img.shields.io/badge/tonal-pitch-yellow.svg)](https://www.npmjs.com/browse/keyword/tonal)

`tonal-pitch` is a low level module to encode and manipulate music pitch and intervals.

This is part of [tonal](https://www.npmjs.com/package/tonal) music theory library.

You can install via npm: `npm i --save tonal-pitch`

## API Reference

<dl>
<dt><a href="#pitch">pitch(fifths, focts, dir)</a> ⇒ <code>Pitch</code></dt>
<dd><p>Create a pitch</p>
</dd>
<dt><a href="#isPitch">isPitch(p)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Test if an object is a pitch</p>
</dd>
<dt><a href="#encode">encode(step, alt, oct, dir)</a></dt>
<dd><p>Encode a pitch</p>
</dd>
<dt><a href="#pType">pType(p)</a> ⇒ <code>String</code></dt>
<dd><p>Get pitch type</p>
</dd>
<dt><a href="#isNotePitch">isNotePitch(p)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Test if is a pitch note (with or without octave)</p>
</dd>
<dt><a href="#isIvlPitch">isIvlPitch(p)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Test if is an interval</p>
</dd>
<dt><a href="#isPC">isPC(p)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Test if is a pitch class (a pitch note without octave)</p>
</dd>
<dt><a href="#fifths">fifths(p)</a> ⇒ <code>Integer</code></dt>
<dd><p>Get encoded fifths from pitch.</p>
</dd>
<dt><a href="#focts">focts(p)</a> ⇒ <code>Integer</code></dt>
<dd><p>Get encoded octaves from pitch.</p>
</dd>
<dt><a href="#height">height(p)</a> ⇒ <code>Integer</code></dt>
<dd><p>Get height of the pitch.</p>
</dd>
<dt><a href="#parseNote">parseNote(str)</a> ⇒ <code>Pitch</code></dt>
<dd><p>Parse a note</p>
</dd>
<dt><a href="#parseIvl">parseIvl(str)</a> ⇒ <code>Pitch</code></dt>
<dd><p>Parse an interval</p>
</dd>
<dt><a href="#parsePitch">parsePitch(str)</a> ⇒ <code>Pitch</code></dt>
<dd><p>Parse a note or an interval</p>
</dd>
<dt><a href="#asNotePitch">asNotePitch(p)</a> ⇒ <code>Pitch</code></dt>
<dd><p>Ensure the given object is a note pitch. If is a string, it will be
parsed. If not a note pitch or valid note string, it returns null.</p>
</dd>
<dt><a href="#asIvlPitch">asIvlPitch(p)</a> ⇒ <code>Pitch</code></dt>
<dd><p>Ensure the given object is a interval pitch. If is a string, it will be
parsed. If not a interval pitch or valid interval string, it returns null.</p>
</dd>
<dt><a href="#asPitch">asPitch(p)</a> ⇒ <code>Pitch</code></dt>
<dd><p>Ensure the given object is a pitch. If is a string, it will be
parsed. If not a pitch or valid pitch string, it returns null.</p>
</dd>
<dt><a href="#strNote">strNote(p)</a> ⇒ <code>String</code></dt>
<dd><p>Convert a note pitch to string representation</p>
</dd>
<dt><a href="#strIvl">strIvl(p)</a> ⇒ <code>String</code></dt>
<dd><p>Convert a interval pitch to string representation</p>
</dd>
<dt><a href="#strPitch">strPitch(p)</a> ⇒ <code>String</code></dt>
<dd><p>Convert a pitch to string representation (either notes or intervals)</p>
</dd>
<dt><a href="#noteFn">noteFn(fn)</a> ⇒ <code>function</code></dt>
<dd><p>Decorate a function to work internally with note pitches, even if the
parameters are provided as strings. Also it converts back the result
to string if a note pitch is returned.</p>
</dd>
<dt><a href="#ivlFn">ivlFn(fn)</a> ⇒ <code>function</code></dt>
<dd><p>Decorate a function to work internally with interval pitches, even if the
parameters are provided as strings. Also it converts back the result
to string if a interval pitch is returned.</p>
</dd>
<dt><a href="#pitchFn">pitchFn(fn)</a> ⇒ <code>function</code></dt>
<dd><p>Decorate a function to work internally with pitches, even if the
parameters are provided as strings. Also it converts back the result
to string if a pitch is returned.</p>
</dd>
</dl>

<a name="pitch"></a>

## pitch(fifths, focts, dir) ⇒ <code>Pitch</code>
Create a pitch

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| fifths | <code>Integer</code> | the number of fifths from C or from P1 |
| focts | <code>Integer</code> | the number of encoded octaves |
| dir | <code>Integer</code> | (Optional) Only required for intervals. Can be 1 or -1 |

<a name="isPitch"></a>

## isPitch(p) ⇒ <code>Boolean</code>
Test if an object is a pitch

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="encode"></a>

## encode(step, alt, oct, dir)
Encode a pitch

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| step | <code>Integer</code> |  |
| alt | <code>Integer</code> |  |
| oct | <code>Integer</code> |  |
| dir | <code>Integer</code> | (Optional) |

<a name="pType"></a>

## pType(p) ⇒ <code>String</code>
Get pitch type

**Kind**: global function  
**Returns**: <code>String</code> - 'ivl' or 'note' or null if not a pitch  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="isNotePitch"></a>

## isNotePitch(p) ⇒ <code>Boolean</code>
Test if is a pitch note (with or without octave)

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="isIvlPitch"></a>

## isIvlPitch(p) ⇒ <code>Boolean</code>
Test if is an interval

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="isPC"></a>

## isPC(p) ⇒ <code>Boolean</code>
Test if is a pitch class (a pitch note without octave)

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="fifths"></a>

## fifths(p) ⇒ <code>Integer</code>
Get encoded fifths from pitch.

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="focts"></a>

## focts(p) ⇒ <code>Integer</code>
Get encoded octaves from pitch.

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="height"></a>

## height(p) ⇒ <code>Integer</code>
Get height of the pitch.

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="parseNote"></a>

## parseNote(str) ⇒ <code>Pitch</code>
Parse a note

**Kind**: global function  
**Returns**: <code>Pitch</code> - the pitch or null if not valid note string  

| Param | Type |
| --- | --- |
| str | <code>String</code> |

<a name="parseIvl"></a>

## parseIvl(str) ⇒ <code>Pitch</code>
Parse an interval

**Kind**: global function  
**Returns**: <code>Pitch</code> - the pitch or null if not valid interval string  

| Param | Type |
| --- | --- |
| str | <code>String</code> |

<a name="parsePitch"></a>

## parsePitch(str) ⇒ <code>Pitch</code>
Parse a note or an interval

**Kind**: global function  
**Returns**: <code>Pitch</code> - the pitch or null if not valid pitch string  

| Param | Type |
| --- | --- |
| str | <code>String</code> |

<a name="asNotePitch"></a>

## asNotePitch(p) ⇒ <code>Pitch</code>
Ensure the given object is a note pitch. If is a string, it will be
parsed. If not a note pitch or valid note string, it returns null.

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> &#124; <code>String</code> |

<a name="asIvlPitch"></a>

## asIvlPitch(p) ⇒ <code>Pitch</code>
Ensure the given object is a interval pitch. If is a string, it will be
parsed. If not a interval pitch or valid interval string, it returns null.

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> &#124; <code>String</code> |

<a name="asPitch"></a>

## asPitch(p) ⇒ <code>Pitch</code>
Ensure the given object is a pitch. If is a string, it will be
parsed. If not a pitch or valid pitch string, it returns null.

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> &#124; <code>String</code> |

<a name="strNote"></a>

## strNote(p) ⇒ <code>String</code>
Convert a note pitch to string representation

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="strIvl"></a>

## strIvl(p) ⇒ <code>String</code>
Convert a interval pitch to string representation

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="strPitch"></a>

## strPitch(p) ⇒ <code>String</code>
Convert a pitch to string representation (either notes or intervals)

**Kind**: global function  

| Param | Type |
| --- | --- |
| p | <code>Pitch</code> |

<a name="noteFn"></a>

## noteFn(fn) ⇒ <code>function</code>
Decorate a function to work internally with note pitches, even if the
parameters are provided as strings. Also it converts back the result
to string if a note pitch is returned.

**Kind**: global function  
**Returns**: <code>function</code> - the decorated function  

| Param | Type |
| --- | --- |
| fn | <code>function</code> |

<a name="ivlFn"></a>

## ivlFn(fn) ⇒ <code>function</code>
Decorate a function to work internally with interval pitches, even if the
parameters are provided as strings. Also it converts back the result
to string if a interval pitch is returned.

**Kind**: global function  
**Returns**: <code>function</code> - the decorated function  

| Param | Type |
| --- | --- |
| fn | <code>function</code> |

<a name="pitchFn"></a>

## pitchFn(fn) ⇒ <code>function</code>
Decorate a function to work internally with pitches, even if the
parameters are provided as strings. Also it converts back the result
to string if a pitch is returned.

**Kind**: global function  
**Returns**: <code>function</code> - the decorated function  

| Param | Type |
| --- | --- |
| fn | <code>function</code> |