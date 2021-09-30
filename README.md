# Engram-es Spanish keyboard layout

Engram-es is a key layout optimized for comfortable and efficient touch typing in Spanish 
created by [Arno Klein](https://binarybottle.com) with help from Ian Douglas, aMiguel Guzmán, and Nick Gutiérrez.
There is [open source code](https://github.com/binarybottle/engram-es)
based on the original English Engram [open source code](https://github.com/binarybottle/engram).
<!-- You can install the engram-es layout on [Windows, macOS, and Linux](https://keyman.com/keyboards/engram)
or [try it out online](https://keymanweb.com/#en,Keyboard_engram).-->

Letters are optimally arranged according to ergonomics factors that promote reduction of lateral finger movements and more efficient typing of high-frequency letter pairs. The most common punctuation marks and special key for diacritical marks (☆) are logically grouped together in the middle columns and numbers are paired with mathematical and logic symbols (shown as pairs of default and Shift-key-accessed characters). See below for a full description.


          [ | = ~ +   <  >   ^ & % * ] \
          ( 1 2 3 4   5  6   7 8 9 0 ) /

            Z H O X  .:  "'  M D B J W -_ @#
            P I E A  ,;  ☆   T S N R K
            F Y Q U  ¿¡  ?!  C L V G
            
    ☆ + aeiouAEIOU = áéíóúÁÉÍÓÚ (acute accent)
    ☆ + nN = ñÑ
    ☆ + cC = çÇ
    ☆ + Shift         + [letter] = [letter] with a diaresis/umlaut: ü
    ☆         + AltGr + [letter] = [letter] with a grave accent: è
    ☆ + Shift + AltGr + [letter] = [letter] with a circumflex: â
    AltGr + ( = { (open curly brace)
    AltGr + ) = } (close curly brace)
    AltGr + 5 = « (open quote/comillas) 
    AltGr + 6 = » (close quote/comillas)
    AltGr + - = — (em dash)
    AltGr + ' = ` (back tick)
    AltGr + . = • (middle dot, or "interpunct")
    AltGr + s = $ (dollar currency)
    AltGr + e = € (euro currency)
    AltGr + l = £ (pound currency)

### Standard diagonal keyboard (default, Shift, and AltGr layers)
![Standard keyboard](https://github.com/binarybottle/engram-es/blob/master/assets/engram-es.png?raw=true)

(c) 2021 Arno Klein, MIT license

----------------

# Contents
1. [Why a new keyboard layout?](#why)
2. [Guiding criteria](#criteria)
3. [Summary of steps and results](#summary)

## Why a new keyboard layout? <a name="why">

**History** <br>
After creating the [English Engram layout](https://engram.dev) ([open source code](https://github.com/binarybottle/engram)), community members came together to help guide the creation of a Spanish version.  Thank you, Nick Gutiérrez (@NickG13) and Miguel Guzmán (@Lobo-Feroz), and a special thanks to Ian Douglas (@iandoug) for cleaning up the Leipzig Spanish corpus and for computing character and bigram frequencies!  For documentation of this Spanish corpus, please see [Creating a Corpus and Chained Bigrams for Spanish Keyboard Development and Evaluation](https://zenodo.org/record/5501931).

**Why "Engram"?** <br>
The name is a pun, referring both to "n-gram", letter permutations and their frequencies that are used to compute the Engram layout, and "engram", or memory trace, the postulated change in neural tissue to account for the persistence of memory, as a nod to my attempt to make this layout easy to remember.
         
## Guiding criteria   <a name="criteria">

    1.  Assign letters to keys that don't require lateral finger movements.
    2.  Promote alternating between hands over uncomfortable same-hand transitions.
    3.  Assign the most common letters to the most comfortable keys.
    4.  Arrange letters so that more frequent bigrams are easier to type.
    5.  Promote little-to-index-finger roll-ins over index-to-little-finger roll-outs.
    6.  Balance finger loads according to their relative strength.
    7.  Avoid stretching shorter fingers up and longer fingers down.
    8.  Avoid using the same finger.
    9.  Avoid skipping over the home row.
    10. Assign the most common punctuation to keys in the middle of the keyboard.
    11. Assign easy-to-remember symbols to the Shift-number keys.
    
### Factors used to compute the engram-es layout <a name="factors">
  - Spanish letter and letter bigram frequency data from a cleaned-up version of the Leipzig Spanish corpus. The largest file was downloaded from each row of the [original version](https://wortschatz.uni-leipzig.de/en/download/Spanish), except for rows specified as not from Spain, and lines containing non-Spanish names and words were removed. 
    <br>
  - **Flow factors** (transitions between ordered key pairs)
         
## Summary of steps and results  <a name="summary">

We will assign letters to keys by choosing the arrangement with the highest score according to our scoring model. However, there are over four hundred septillion, or four hundred trillion trillion (26! = 403,291,461,126,605,635,584,000,000, or 4.032914611 E+26) possible arrangements of 26 letters (24! = 6.204484017 E+23), so we will arrange the letters in four steps, based on ergonomics principles. These consist of (Step 1) assigning the eight most frequent letters to different keys, optimizing assignment of the remaining (Step 2) eight most frequent letters, and (Step 3) eight least frequent letters (besides W and K), and (Step 4) exchanging letters. 

## Step 1: Define the shape of the key layout to minimize lateral finger movements

We will assign 24 letters to 8 columns of keys separated by two middle columns reserved for punctuation. These 8 columns require no lateral finger movements when touch typing, since there is one column per finger. The most comfortable keys include the left and right home rows (keys 5-8 and 17-20), the top-center keys (2,3 and 14,15) that allow the longer middle and ring fingers to uncurl upwards, as well as the bottom corner keys (9,12 and 21,24) that allow the shorter fingers to curl downwards. We will assign the two least frequent letters, W and K, to the two hardest-to-reach keys lying outside the 24-key columns in the upper right (25 and 26):

        Left:            Right:
     1  2  3  4       13 14 15 16 25
     5  6  7  8       17 18 19 20 26
     9 10 11 12       21 22 23 24

We will consider the most comfortable keys to be those typed by either hand on the home row, by the ring and middle finger above the home row, and by the index and little finger below the home row, with a preference for the strongest (index and middle) fingers:
    
     -  2  3  -        - 14 15  -  
     5  6  7  8       17 18 19 20  
     9  -  - 12       21  -  - 24
         
## Step 2: Arrange the most frequent letters based on comfort and bigram frequencies  <a name="step2">

Below, we will arrange vowels on one side and the most frequent consonants to the other side to encourage balance and alternation across hands. Since aside from the letters W and K there is symmetry across left and right sides, we will decide later which side the vowels and which side the most frequent consonants should go.

### Vowels
    
**E, A, O**, S, N, **I**, R, L, D, C, T, U, M, P, B, G, V, Q, Y, F, H, J, Z, X, K, W
                         
Bigrams that contain two non-repeating vowels, and their frequencies:
  
    UE	17135545
    IO	10629390
    IA	 9704625
    IE 	 8264649
    UA	 2727622
    UI	 2699510
    EA   1634965
    AU   1206620
    EO	  787382
    AI	  768894
    EI	  578063
    EU	  338775
    IU	  314965
    AE	  279633
    OI	  193436
    OE	  182266
    UO	  175574
    OU	  174475
    OA	  117839
    AO	   88065
  
We will assign the most frequent vowels (E=294897235, A=271738665, O=201996963, I=151438547) to four of the six most comfortable keys on the left side of the keyboard (keys 2,3,5,6,7,8). We will assign the letter E, the most frequent in the Spanish language, to the strongest (middle) finger on the home row, and assign the other three vowels such that (1) the home row keys typed by the index and middle fingers are not left vacant, and any top-frequency bigram (more than 1 million instances) (2) does not use the same finger and (3) reads from left to right (ex: UE, not EU) for ease of typing (inward roll from little to index finger vs. outward roll from index to little finger). These constraints lead to 4 arrangements of the 4 vowels:

    - - O -    - - O -    - O - -    - - - -    
    - I E A    I - E A    I - E A    I O E A
    - - - -    - - - -    - - - -    - - - -

### Consonants

E, A, O, **S, N**, I, **R, L, D, C, T**, U, M, P, B, G, V, Q, Y, F, H, J, Z, X, K, W

On the right side of the keyboard, we will assign four of the seven most frequent consonants (S=162205879, N=161440601, R=147218050, L=124544026, D=113430944, C=99562807, T=99294129) to the four home row keys. We will assign the letter S, the most frequent consonant in the Spanish language, to the strongest (middle) finger on the home row.
    
Bigrams that contain two non-repeating consonants, with frequencies greater than 1 million:

    NT	13403852
    ST	10479844
    TR   6982844
    ND	 6501402
    PR	 5241844
    NC	 4535985
    RT	 3473930
    BR	 3216626
    MP	 3063320
    CH	 2911020
    SP	 2412701
    NS	 2352231
    MB	 2169462
    GR	 2082624
    BL	 2053224
    CT	 1927284
    RM	 1908571
    SC	 1907706
    CR	 1537677
    RD	 1524597
    RS	 1509084
    PL	 1459569
    RC	 1280075
    NG	 1253772
    LT	 1253199
    DR	 1140387
    RN	 1072129
    RG	 1017226

Bigrams from the above list that contain two of the most frequent consonants (S, N, R, L, D, C, T):
    
    NT	13403852
    ST	10479844
    TR   6982844
    ND	 6501402
    NC	 4535985
    RT	 3473930
    NS	 2352231
    CT	 1927284
    SC	 1907706
    CR	 1537677
    RD	 1524597
    RS	 1509084
    RC	 1280075
    LT	 1253199
    DR	 1140387
    RN	 1072129

As with the left side, letters are placed so that top-frequency bigrams read from right to left (ex: "NT" read as TN, not NT) except when both sequences have more than 1 million instances (TR/RT, CR/RC, and RD/DR), for ease of typing. The above constraints lead to 4 arrangements of the consonants:

    - - - -    - - - -    - - - -    - - - -
    L S N R    D S N R    C S N R    T S N R
    - - - -    - - - -    - - - -    - - - -

The resulting 16 initial layouts, each with 16 unassigned keys, are represented below with the three rows on the left and right side of the keyboard as a linear string of letters, with unassigned keys denoted by “-”.
    
    Pattern 1:
    
    --O- -IEA ----    ---- LSNR ----
    --O- -IEA ----    ---- DSNR ----
    --O- -IEA ----    ---- CSNR ----
    --O- -IEA ----    ---- TSNR ----

    Pattern 2:
    
    --O- I-EA ----    ---- LSNR ----
    --O- I-EA ----    ---- DSNR ----
    --O- I-EA ----    ---- CSNR ----
    --O- I-EA ----    ---- TSNR ----

    Pattern 3:
    
    -O-- I-EA ----    ---- LSNR ----
    -O-- I-EA ----    ---- DSNR ----
    -O-- I-EA ----    ---- CSNR ----
    -O-- I-EA ----    ---- TSNR ----

    Pattern 4:
    
    ---- IOEA ----    ---- LSNR ----
    ---- IOEA ----    ---- DSNR ----
    ---- IOEA ----    ---- CSNR ----
    ---- IOEA ----    ---- TSNR ----    

## Step 3: Optimize assignment of the remaining letters <a name="step3">
    
We want to assign letters to the 16 unassigned keys in each of the above 16 layouts based on our scoring model. That would mean scoring all possible arrangements for each layout and choosing the arrangement with the highest score, but since there are over 20 trillion (16!) possible ways of arranging 16 letters, we will break up the assignment into two stages for the most frequent and least frequent remaining letters. 
    
### Most frequent letters
We will compute scores for every possible arrangement of the seven most frequent of the remaining letters (in bold below) assigned to vacancies among the most comfortable sixteen keys.

E, A, O, S, N, I, R, **L, D, C, T, U, P, M, B, G**, V, Q, H, F, Y, J, Z, X, K, W

        Left:            Right:
     -  2  3  -        - 14 15  -
     5  6  7  8       17 18 19 20
     9  -  - 12       21  -  - 24

Since there are 40,320 (8!) possible combinations of eight letters for each of the 16 layouts, we need to score and evaluate 645,120 layouts. To score each arrangement of letters, we construct a frequency matrix where we multiply a matrix containing the frequency of each ordered pair of letters (bigram) by our flow and strength matrices to compute a score.
    
### Least frequent letters
Next we will compute scores for every possible (40,320 = 8!) arrangement of the least frequent eight letters (in bold below, besides W and K) in the remaining keys, after substituting in the 16 top results of the above, for another 645,120 layouts:

E, A, O, S, N, I, R, L, D, C, T, U, P, M, B, G, **V, Q, H, F, Y, J, Z, X**, K, W

        Left:            Right:
     1  -  -  4       13  -  - 16
     -  -  -  -        -  -  -  -
     - 10 11  -        - 22 23  -
     
#### Further optimize layouts by exchanging more letters

If we relax the above fixed initializations and permit further exchange of letters, then we can search for even higher-scoring layouts. As a final optimization step we exchange letters, eight keys at a time (8! = 40,320) selected twice in 14 different ways, in each of the above 16 layouts, to score a total of over 18 million combinations. We allow the following keys to exchange letters:

    1. Top rows
    2. Bottom rows
    3. Top and bottom rows on the right side
    4. Top and bottom rows on the left side
    5. Top right and bottom left rows
    6. Top left and bottom right rows
    7. Center of the top and bottom rows on both sides
    8. The eight corners
    9. Left half of the top and bottom rows on both sides
    10. Right half of the top and bottom rows on both sides
    11. Left half of non-home rows on the left and right half of the same rows on the right
    12. Right half of non-home rows on the left and left half of the same rows on the right
    13. Top center and lower sides
    14. Top sides and lower center
    15. Repeat 1-14
         
### Create variants of top-scoring layouts

As an alternative to simply choosing the first-place layout, we can generate variations of this layout and find those variants within a small difference of one another and select from among these variants. For this, we select keys to vary, compute scores for every combination of the letters assigned to these keys, and select among those that are tied for first place.
         
## **Engram Scoring Model**
    
Our optimization algorithm finds every permutation of a given set of letters, maps these letter permutations to a set of keys, and ranks these letter-key mappings according to a score reflecting ease of typing key pairs and frequency of letter pairs (bigrams). The score is the average of the scores for all possible bigrams in this arrangement. The score for each bigram is a product of the frequency of occurrence of that bigram, the frequency of each of the bigram’s characters, and flow, strength (and optional speed) factors for the key pair.
    
#### Factors to penalize strenuous key transitions

Direction:
    
    - outward = 0.9: outward roll of fingers from the index to little finger (same hand)

Dexterity:
    
    - side_above_3away = 0.9
        - index and little finger type two keys, one or more rows apart (same hand)
    - side_above_2away = 0.9^2 = 0.81
        - index finger types key a row or two above ring finger key, or
        - little finger types key a row or two above middle finger key (same hand)
    - side_above_1away = 0.9^3 = 0.729
        - index finger types key a row or two above middle finger key, or
        - little finger types key a row or two above ring finger key (same hand)
    - middle_above_ring = 0.9
        - middle finger types key a row or two above ring finger key (same hand)
    - ring_above_middle = 0.9^3 = 0.729
        - ring finger types key a row or two above middle finger key (same hand)
    - lateral = 0.9
        - lateral movement of (index or little) finger outside of 8 vertical columns
    
Distance:
    
    - skip_row_3away = 0.9       
        - index and little fingers type two keys that skip over home row (same hand)
        - (e.g., one on bottom row, the other on top row)
    - skip_row_2away = 0.9^3 = 0.729
        - little and middle or index and ring fingers type two keys that skip over home row (same hand)
    - skip_row_1away = 0.9^5 = 0.59049
        - little and ring or middle and index fingers type two keys that skip over home row (same hand)

Repetition:
 
    - skip_row_0away = 0.9^4 = 0.6561
        - same finger types two keys that skip over home row
    - same_finger = 0.9^5 = 0.59049
        - use same finger again for a different key
        - cannot accompany outward, side_above, or adjacent_shorter_above 

Strength: Accounted for by the strength matrix (minimum value for the little finger = 0.9) 

## Step 4: Evaluate winning layout <a name="step4">
    
We evaluate the candidate winner with tests:
    
    1. Evaluate variants of the candidate winner using interkey speed estimates
    2. Evaluate sensitivity of the variants to the scoring parameters
    3. Search for higher-scoring layouts by rearranging letters
         
## Step 5: Arrange non-letter characters in easy-to-remember places <a name="step5">
    
Now that we have all 26 letters accounted for, we turn our attention to non-letter characters, taking into account frequency of punctuation and ease of recall.
  
### Add diacritical marks

A special diacritical key (denoted by ☆ U+2606) when simultaneously pressed with a letter adds a diacritical mark to that letter:
  
    ☆ + aeiouAEIOU = áéíóúÁÉÍÓÚ (acute accent)
    ☆ + nN = ñÑ
    ☆ + cC = çÇ
    ☆ + Shift + [letter] = [letter] with a diaresis/umlaut: ü
    
For generalizability beyond Spanish:
    
    ☆         + AltGr + [letter] = [letter] with a grave accent: è
    ☆ + Shift + AltGr + [letter] = [letter] with a circumflex: â
 

### Add punctuation keys and number keys

We will assign some of the most frequent punctuation to the six keys in the middle two columns:

            Z H O X  .   "   M D B J W
            P I E A  ,   ☆   T S N R K
            F Y Q U  ¿   ?   C L V G

We will use the Shift key to group similar punctuation marks:

            Z H O X  .:  "'  M D B J W
            P I E A  ,;  ☆   T S N R K
            F Y Q U  ¿¡  ?!  C L V G

**Number keys**: 
The numbers are flanked to the left and right by [square brackets], and {curly brackets} accessed by the Shift key. Each of the numbers is paired with a mathematical or logic symbol accessed by the Shift key:
    
    { | = ~ +   <  >   ^ & % * } \
    [ 1 2 3 4   5  6   7 8 9 0 ] /

    1: | (vertical bar or "pipe" represents the logical OR operator: 1 stroke, looks like the number one)
    2: = (equal: 2 strokes, like the Chinese character for "2")
    3: ~ (tilde: "almost equal", often written with 3 strokes, like the Chinese character for "3")
    4: + (plus: has four quadrants; resembles "4")
    5 & 6: < > ("less/greater than"; these angle brackets are directly above the other bracket keys)
    7: ^ (caret for logical XOR operator as well as exponentiation; resembles "7")
    8: & (ampersand: logical AND operator; resembles "8")
    9: % (percent: related to division; resembles "9")
    0: * (asterisk: for multiplication; resembles "0") 

The three remaining keys in many common keyboards (flanking the upper right hand corner Backspace key) are displaced in special keyboards, such as the Kinesis Advantage and Ergodox. For the top right key, we will assign the forward slash and backslash: / \\. For one of the remaining two keys we will assign the hyphen and underscore, and to the other key, two symbols that in modern usage have significance in social media: the hash/pound sign and the "at sign". The hash or hashtag identifies digital content on a specific topic (the Shift key accesses the money sign). The "at sign" identifies a location or affiliation (such as in email addresses) and acts as a "handle" to identify users in popular social media platforms and online forums.

The resulting engram-es layout:

          [ | = ~ +   <  >   ^ & % * ] \
          ( 1 2 3 4   5  6   7 8 9 0 ) /

            Z H O X  .:  "'  M D B J W -_ @#
            P I E A  ,;  ☆   T S N R K
            F Y Q U  ¿¡  ?!  C L V G

The AltGr key will access additional symbols:
    
    AltGr + ( = { (open curly brace)
    AltGr + ) = } (close curly brace)
    AltGr + 5 = « (open quote/comillas) 
    AltGr + 6 = » (close quote/comillas)
    AltGr + - = — (em dash)
    AltGr + ' = ` (back tick)
    AltGr + . = • (middle dot, or "interpunct")
    AltGr + s = $ (dollar currency)
    AltGr + e = € (euro currency)
    AltGr + l = £ (pound currency)
 
And the extra key on ISO keyboards accesses a duplicate asterisk (*).
