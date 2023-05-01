---
author: Peter Jonson
title: Regular Expressions
description: Regular Expressions
draft: false
tags: ['Regular Expressions']
date: 2022-09-24
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

A regular expression, regex or regexp (sometimes called a rational expression) is, in theoretical computer science and formal language theory, a sequence of characters that define a search pattern. Usually this pattern is then used by string searching algorithms for "find" or "find and replace" operations on strings, or for input validation.

Source: Wikipedia

<table cellpadding="4">
<tr>
<th> Character
</th>
<th> Description
</th></tr>
<tr>
<td> <b>^</b>
</td>
<td> A circumflex at the start of the string matches the start of a line.
</td></tr>
<tr>
<td> <b>$</b>
</td>
<td> A dollar sign at the end of the expression matches the end of a line.
</td></tr>
<tr>
<td> <b>.</b>
</td>
<td> A period matches a single instance of any character. For example, b.t matches <i>bot</i>, and <i>bat</i>, but not <i>boat</i>.
</td></tr>
<tr>
<td> <b>?</b>
</td>
<td> A question mark after a character or a character group matches zero or one occurrences of that character or group. For example, bo?t matches both <i>bt</i> and <i>bot</i>.
</td></tr>
<tr>
<td> <b>*</b>
</td>
<td> An asterisk after a character or a character group matches any number of occurrences of that character or group, including zero occurrences. For example, bo*t matches <i>bt</i>, <i>bot</i>, and <i>boot</i>.
</td></tr>
<tr>
<td> <b>+</b>
</td>
<td> A plus sign after a character or a character group matches any number of occurrences of that character or a character group, with at least one occurrence. For example, bo+t matches <i>bot</i> and <i>boot</i>, but not <i>bt</i>.
</td></tr>
<tr>
<td> <b>|</b>
</td>
<td> A vertical bar matches each expression on each side of the vertical bar. For example, bar|car will match either <i>bar</i> or <i>car</i>.
</td></tr>
<tr>
<td> <b>[ ]</b>
</td>
<td> Characters inside square brackets match any character that appears in the brackets, but no others. For example, [bot] matches <i>b</i>, <i>o</i>, or <i>t</i>.
</td></tr>
<tr>
<td> <b>[^]</b>
</td>
<td> A circumflex at the start of a string inside square brackets means NOT. Hence, [^bot] matches any characters except <i>b</i>, <i>o</i>, or <i>t</i>.
</td></tr>
<tr>
<td> <b>[-]</b>
</td>
<td> A hyphen inside square brackets signifies a range of characters.
<p>For example, [b-o] matches any character from <i>b</i> through <i>o</i>.
</p>
</td></tr>
<tr>
<td> <b>{ }</b>
</td>
<td> Braces group characters or expressions. Groups can be nested, with a maximum number of 10 groups in a single pattern. For the Replace operation, groups are referred to by a backslash and a number, according to the position in the "Text to find" expression, beginning with 0. For example, given the text to find and replacement strings, Find: {[0-9]}{[a-c]*}, Replace: NUM\1, the string 3abcabc is changed to NUMabcabc.
</td></tr>
<tr>
<td> <b>( )</b>
</td>
<td> Parenthesis are an alternative to braces (<b>{ }</b>), with the same behavior.
</td></tr>
<tr>
<td> <b>\</b>
</td>
<td> A backslash before a wildcard character tells the Code Editor to treat that character literally, not as a wildcard. For example, \^ matches ^ and does not look for the start of a line.
</td></tr></table>

{{< aetl >}}
