# ngram-keychords

Deciding appropriate letter-pairs we can use for keychording seems a daunting task, but by analyzing Google's N-Gram datasets, we can find the *least common* key-pairings in the English language, and avoid conflicts.

This isn't infallible; the pair "dk" seems to be infrequent enough to include in the list of preferable chord-pairs, but if you type "mkdir", "weekday" (!), or "bodkin" enough, your prose will eventually collide with a command.

I've included a list of keypairings I've bound to commands, along with some commentary about their utility, but if you want to do your own analysis, check out the datasets themselves:

Google N-Gram Datasets
https://storage.googleapis.com/books/ngrams/books/datasetsv2.html

My preferred Emacs chording package is keychord.el, as demonstrated in

Emacs Rocks! Episode 7
http://emacsrocks.com/e07.html

The way you bind the command to a keychord using this package is:

`(key-chord-define-global "fj" 'delete-local-region)`

Here is the list of keychords I currently use:
```
;; Home row to number row keybindings are too stretchy
;; Numrow to numrow conflicts with *actual* number entry.

;; ;; Left-hand numrow chords

;;Natural toprow and numrow
"e1"
"e2"

"r2"
"r3"

"t3"
"t4"

;; Inverted toprow and numrow (only q is acceptable, ime)
"q3"
"q4"

"w4"
"w5"

"e5"
"e6"

;; Slightly awkward close pairings
"q1"
"w2"
"e3"
"r4"
"t5"

;; ;; Right-hand numrow chords
;; Home row to number row too stretchy
;; Numrow to numrow conflicts with *actual* number entry.

;; Natural toprow and numrow
"u9"
"u0"

"y8"
"y9"

"i0"
"i-"

"o-"
"o="

;; Inverted toprow and numrow (only [ is acceptable, ime)
"[-"
"[0"

"p9"
"p8"

"o8"
"o7"

;; Slightly awkward close pairings
"y7"
"u8"
"i9"
"o0"
"p-"

"jk"
"kk"
"jl"
"jj"

"hk"
"hj"

"fg"
"fb"

"hb"
"hh"

"zj"
"zn"

"gj"
"gk" ; maybe conflict? had this commented out
"dj"

"fj" ; I use this for 'delete-local-region
"vv" ; I use this to kill-line and leave a new line

"vj"
"vh"

"vk"
"vm"
"vb"

"qw"
"qr"
"qp"

"qq"

"xq" ; awkward

"xh"
"zh"
"xx"
"zg"

"vf"
"zx" ; awkward

"xj"
"xk"

"bg" ; awkward

"xg"
"xb"

"qk"

"jt"

"yy"
"uu"

"cv"
"xv"
```
