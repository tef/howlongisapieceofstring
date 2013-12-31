# A draft. Don't link.

Things I want to cover

- encodings vs character sets
- potted history
- character encodings, c
- fixed and variable width encodings
- combining characters
- normalization
- casefolding
- unicode sandwich, nedbat
- joel’s overview
- unicode love hotel
- han unification
- unicode 88
- utf-8 vs cebu/utf-8 and a half
- spotify's unicode bug
- mojibake

# How long is a piece of string? A Unicode Survival Guide

Unicode has become the de-facto way to encode human text into a series of ones and zeroes, for most of the written languages in common use by humans today. Unfortunately, programmers are now expected to understand a considerable amount of how human languages work, and ideally forget much of what they assume to be true about languages in general.

For those who are impatient, here are some faulty, broken assumptions about text you can use in lieu of your existing ones. They will get you through most of th nightmares of truly handling human input, but you're still going to have to learn a bit, chump.

## Don't Panic.

- Handle decoding and encoding at the edge of your program, use unicode strings internally. Colloquially this is known as a unicode sandwich
- When in doubt, read and write text using UTF-8. Your internals mightuse a different representation, though.
- Treat unicode as an opaque blob. Avoid cutting it up into words, characters, or sentences. Don't try and transform it into lower or  upper case either.
- You will need to normalize strings before comparing them. There is always more than one way to represent text inside unicode.

## A brief history of language on computers

Let's ignore EBCDIC, because if you're having to use it, you are already past salvition. ASCII seems a good place to start, or let's hammer most of the latin alphabet, and mash some punctuation into one hundred and twenty eight numbered slots. 

ASCII is a mixture of lesser known control characters, upper and lower A-Z, numbers, and punctuation. It also found the time to invent punctuation, like the backslash, inbetween turning all dashes and quotes into homogenous blobs.

One bit short of a byte, it left some room for people to mash in extra characters when needed.

## Unicode 88

The clusterfuck left in the wake of ASCII took a lot of time to sort out. Every country and computer packed their own special selection of characters into those remaining 128 slots.

Something had to be done, well, it would be nice to be able to use different languages in the same document without crying, and so unicode happened.

## Fixed and Variable Width Encodings

## Combining Characters.

## Surrogate Pairs

## UTF-8½, or when UTF-8 isn't. 

## Casefolding

## Normalization.

## Unicode is social before it is technical.

Splitting words? Sorting? Han unification? Love hotel & Emoji.
