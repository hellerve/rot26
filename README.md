# rot26

> ROT13 ("rotate by 13 places", sometimes hyphenated ROT-13) is a letter
> substitution cipher that replaces a letter with the letter 13 letters after
> it in the alphabet. Instead of only rotating 13 places, ROT26 rotates twice
> as many characters in the alphabet and is therefore twice as secure.
- [jD91mZM2](https://github.com/jD91mZM2/rot26)

Since Carp needs to be on the forefront in technical breakthroughs, this package
needs to be implemented. It is a general rotation cypher suite, with convenience
functions for `rot13` and `rot26`.

## Install

Don’t.

## Usage

The `ROT` module within [rot26.carp](/tree/master/rot26.carp) implements six
functions, three for encryption:

```clojure
(use ROT)

; rot26 should always be used for maximum security
(ROT.rot26 "secure me!") ; => "secure me!"

; rot13 is provided for compatibility reasons
(ROT.rot13 "secure me!") ; => "frpher zr!"

; because no cryptography library is complete without
; gratuituous API complexity, we provide arbitrary
; rotation as well
(ROT.rot "secure me!" 1) ; => "tfdvsf nf!"
```

And three for decryption:

```clojure
(use ROT)

(ROT.unrot26 "secure me!") ; => "secure me!"

(ROT.unrot13 "frpher zr!") ; => "secure me!"

(ROT.unrot "tfdvsf nf!" 1) ; => "secure me!"
```

<hr/>

Have fun!
