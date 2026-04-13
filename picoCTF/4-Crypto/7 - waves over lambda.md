### waves over lambda
We made a lot of substitutions to encrypt this. Can you decrypt it?Connect with nc fickle-tempest.picoctf.net 51558.
### Solución
Entramos a la conexión dada y obtenemos un cifrado por sustitucion.
```
-------------------------------------------------------------------------------
ewoiznla fbzb ta jwcz srni - szbdcboej_ta_e_whbz_rnupyn_p613b7yy
-------------------------------------------------------------------------------
qb qbzb owl ucef uwzb lfno n dcnzlbz ws no fwcz wcl ws wcz aftv ltrr qb anq fbz atom, noy lfbo t coybzalwwy swz lfb stzal ltub qfnl qna ubnol pj n aftv swcoybztoi to lfb abn.  t ucal nemowqrbyib t fny fnzyrj bjba lw rwwm cv qfbo lfb abnubo lwry ub afb qna atomtoi; swz szwu lfb uwubol lfnl lfbj znlfbz vcl ub tolw lfb pwnl lfno lfnl t utifl pb anty lw iw to, uj fbnzl qna, na tl qbzb, ybny qtlfto ub, vnzlrj qtlf sztifl, vnzlrj qtlf fwzzwz ws utoy, noy lfb lfwcifla ws qfnl qna jbl pbswzb ub.
```
Lo pasamos a un breaker de sustitucion y obtenemos la bandera.
https://www.guballa.de/substitution-solver
frequency_is_c_over_lambda_b613e7dd
### Notas
A substitution cipher is ==a method of encryption where units of plaintext (letters, pairs) are replaced with ciphertext (symbols, other letters) based on a fixed key==. It is one of the oldest, simplest, and most common classical cryptography techniques, often used in recreational puzzles and historical communication.
