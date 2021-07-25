# Arno's engram-es keyboard layout

Engram-es is a key layout optimized for comfortable and efficient touch typing in Spanish 
created by [Arno Klein](https://binarybottle.com), 
with [open source code](https://github.com/binarybottle/engram-es),
based on the original English Engram [open source code](https://github.com/binarybottle/engram).
<!-- You can install the engram-es layout on [Windows, macOS, and Linux](https://keyman.com/keyboards/engram)
or [try it out online](https://keymanweb.com/#en,Keyboard_engram).-->
An article is under review (see the [preprint](https://www.preprints.org/manuscript/202103.0287/v1) that describes the approach).

Letters are optimally arranged according to ergonomics factors that promote reduction of lateral finger movements and more efficient typing of high-frequency letter pairs. The most common punctuation marks are logically grouped together in the middle columns and numbers are paired with mathematical and logic symbols (shown as pairs of default and Shift-key-accessed characters).

<!--
         [{ 1| 2= 3~ 4+  5<  6>  7^ 8& 9% 0* ]} /\
            bB yY oO uU  '(  ")  lL dD wW VV zZ #$ @`
            cC iI eE aA  ,;  .:  hH tT sS nN qQ 
            gG xX jJ kK  -_  ?!  rR MM fF pP            
-->

See below for a full description and comparisons with other key layouts.

<!-- ### Standard diagonal keyboard (default and Shift-key layers)
![Standard keyboard](https://github.com/binarybottle/engram/blob/master/assets/engram-800px.png?raw=true)

### "Ergonomic" orthonormal keyboard (default and Shift-key layers)
![Orthonormal keyboard](https://github.com/binarybottle/engram/blob/master/assets/engram-ergo-squeezed-800px.png?raw=true) -->

(c) 2021 Arno Klein, MIT license

----------------

# Contents
1. [Why Engram?](#why)
2. [Guiding criteria](#criteria)
3. [Summary of steps and results](#summary)

## Why a new key layout? <a name="why">

**Personal history** <br>
In the future, I hope to include an engaging rationale for why I took on this challenge.
Suffice to say I love solving problems, and I have battled repetitive strain injury 
ever since I worked on an old DEC workstation at the MIT Media Lab while composing 
my thesis back in the 1990s.
I have experimented with a wide variety of human interface technologies over the years --
voice dictation, one-handed keyboard, keyless keyboard, foot mouse, and ergonomic keyboards 
like the Kinesis Advantage and [Ergodox](https://configure.ergodox-ez.com/ergodox-ez/layouts/APXBR/latest/0) keyboards with different key switches.
While these technologies can significantly improve comfort and reduce strain, 
if you have to type on a keyboard, it can only help to use a key layout optimized according to sound ergonomics principles. 

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
    
### Factors used to compute the Engram layout <a name="factors">
  - **N-gram letter frequencies** <br>
    
    [Spanish letter and bigram frequency data](http://practicalcryptography.com/cryptanalysis/letter-frequencies-various-languages/spanish-letter-frequencies/)
  - **Flow factors** (transitions between ordered key pairs) <br>
    These factors are influenced by Dvorak's 11 criteria (1936).
    
## Summary of steps and results  <a name="summary">

We will assign letters to keys by choosing the arrangement with the highest score according to our scoring model. However, there are over four hundred septillion, or four hundred trillion trillion (26! = 403,291,461,126,605,635,584,000,000, or 4.032914611 E+26) possible arrangements of 26 letters (24! = 6.204484017 E+23), so we will arrange the letters in four steps, based on ergonomics principles. These consist of (Step 1) assigning the eight most frequent letters to different keys, optimizing assignment of the remaining (Step 2) eight most frequent letters, and (Step 3) eight least frequent letters (besides Z and Q), and (Step 4) exchanging letters. 

### Step 1: Define the shape of the key layout to minimize lateral finger movements

We will assign 24 letters to 8 columns of keys separated by two middle columns reserved for punctuation. These 8 columns require no lateral finger movements when touch typing, since there is one column per finger. The most comfortable keys include the left and right home rows (keys 5-8 and 17-20), the top-center keys (2,3 and 14,15) that allow the longer middle and ring fingers to uncurl upwards, as well as the bottom corner keys (9,12 and 21,24) that allow the shorter fingers to curl downwards. We will assign the two least frequent letters, Z and Q (or J), to the two hardest-to-reach keys lying outside the 24-key columns in the upper right (25 and 26):

        Left:            Right:
     1  2  3  4       13 14 15 16 25
     5  6  7  8       17 18 19 20 26
     9 10 11 12       21 22 23 24

We will consider the most comfortable keys to be those typed by either hand on the home row, by the ring and middle finger above the home row, and by the index and little finger below the home row, with a preference for the strongest (index and middle) fingers:
    
     -  2  3  -        - 14 15  -  
     5  6  7  8       17 18 19 20  
     9  -  - 12       21  -  - 24
     
### Step 2: Arrange the most frequent letters based on comfort and bigram frequencies

Below, we will arrange vowels on one side and the most frequent consonants to the other side to encourage balance and alternation across hands. Since aside from the letters K and W there is symmetry across left and right sides, we will decide later which side the vowels and which side the most frequent consonants should go.

#### Vowels
    
**E, A, O**, S, N, **I**, R, L, D, C, T, U, P, M, B, G, V, Q, H, F, Y, J, Z, X, K, W
                         
The highest frequency bigrams that contain two vowels with more than 100,000 instances:

    UE  985764
    IO  796173
    IA  631386
    IE  490356
    AE  369819
    EA  338302
    OE  317708
    OA  229658
    AU  180953
    UA  163664
    UI  151905
    EU  150552
    AI  147221
    AO  105185
    
We will assign the most frequent vowels (E=10912000, A=10301872, O=7398419, I=5694616) to four of the six most comfortable keys on the left side of the keyboard (keys 2,3,5,6,7,8). We will assign the letter E, the most frequent in the Spanish language, to either of the strongest (index and middle) fingers on the home row, and assign the other three vowels such that (1) the home row keys typed by the index and middle fingers are not left vacant, and any top-frequency bigram (more than 40,000 instances, 1/50th of the highest, DE) (2) does not use the same finger and (3) reads from left to right (ex: UE, not EU) for ease of typing (inward roll from little to index finger vs. outward roll from index to little finger). These constraints lead to eight arrangements of the four vowels:

    - - O -    - - O -    - O - -    - - - -    
    - I A E    I - A E    I - A E    I O A E
    - - - -    - - - -    - - - -    - - - -

    - - O -    - - O -    - O - -    - - - -    
    - I E A    I - E A    I - E A    I O E A
    - - - -    - - - -    - - - -    - - - -

#### Consonants

E, A, O, **S, N**, I, **R, L, D**, C, T, U, P, M, B, G, V, Q, H, F, Y, J, Z, X, K, W

On the right side of the keyboard, we will assign four of the five most frequent consonants (S=6128524, N=5838540, R=5450913, L=4808679, and D=4237020) to the four home row keys. We will assign the letter S, the most frequent consonant in the Spanish language, to either of the strongest (index and middle) fingers on the home row. As with the left side, letters are placed so that top-frequency bigrams (more than 100,000 instances) read from right to left (ex: ND, not DN) for ease of typing: 

    ND  526709 
    SD  485361
    NS  288679   
    NL  233697
    RD  183487       
    LD  162178   
    RS  153332
    RL  147398
    SL  124408
    RN  102872
    
The above constraints lead to two arrangements of the consonants:

    - - - -    - - - -
    D S N R    L S N R
    - - - -    - - - -

We will assign the fifth consonant to a vacant key on the left home row if there is a vacancy, otherwise to the key above the left middle finger. The resulting 16 initial layouts, each with 15 unassigned keys, are represented below with the three rows on the left and right side of the keyboard as a linear string of letters, with unassigned keys denoted by “-”.
    
    --O- LIAE ----    ---- DSNR ----
    --O- LIEA ----    ---- DSNR ----
    --O- ILAE ----    ---- DSNR ----
    --O- ILEA ----    ---- DSNR ----
    -O-- ILAE ----    ---- DSNR ----
    -O-- ILEA ----    ---- DSNR ----
    --L- IOAE ----    ---- DSNR ----
    --L- IOEA ----    ---- DSNR ----
    --O- DIAE ----    ---- LSNR ----
    --O- DIEA ----    ---- LSNR ----
    --O- IDAE ----    ---- LSNR ----
    --O- IDEA ----    ---- LSNR ----
    -O-- IDAE ----    ---- LSNR ----
    -O-- IDEA ----    ---- LSNR ----
    --D- IOAE ----    ---- LSNR ----
    --D- IOEA ----    ---- LSNR ----
    
### Step 3: Optimize assignment of the remaining letters <a name="step3">
    
We want to assign letters to the 15 unassigned keys in each of the above 16 layouts based on our scoring model. That would mean scoring all possible arrangements for each layout and choosing the arrangement with the highest score, but since there are over 1.3 trillion (15!) possible ways of arranging 15 letters, we will break up the assignment into two stages for the most frequent and least frequent remaining letters. 
    
#### Most frequent letters
We will compute scores for every possible arrangement of the seven most frequent of the remaining letters (in bold below) assigned to vacancies among the most comfortable sixteen keys.

E, A, O, S, N, I, R, L, D, **C, T, U, P, M, B, G**, V, Q, H, F, Y, J, Z, X, K, W

        Left:            Right:
     -  2  3  -        - 14 15  -
     5  6  7  8       17 18 19 20
     9  -  - 12       21  -  - 24

Since there are 5,040 (7!) possible combinations of eight letters for each of the 16 layouts, we need to score and evaluate 80,640 layouts. To score each arrangement of letters, we construct a frequency matrix where we multiply a matrix containing the frequency of each ordered pair of letters (bigram) by our flow and strength matrices to compute a score.
    
#### Least frequent letters
Next we will compute scores for every possible (40,320 = 8!) arrangement of the least frequent eight letters (in bold below, besides K and W) in the remaining keys, after substituting in the 16 results of the above for an additional 645,120 layouts:

E, A, O, S, N, I, R, L, D, C, T, U, P, M, B, G, **V, Q, H, F, Y, J, Z, X**, K, W

        Left:            Right:
     1  -  -  4       13  -  - 16
     -  -  -  -        -  -  -  -
     - 10 11  -        - 22 23  -
     
#### Further optimize layouts by exchanging more letters

If we relax the above fixed initializations and permit further exchange of letters, then we can search for even higher-scoring layouts. As a final optimization step we exchange letters, eight keys at a time (8! = 40,320) selected twice in 14 different ways, in each of the above 16 layouts, to score a total of over 18 million more combinations. We allow the following keys to exchange letters:

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
    
### **Engram Scoring Model**
    
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

### Step 4: Evaluate winner against other optimized layouts

<!--
After assigning letters K and W to upper right keys outside of the home blocks and testing left/right side swap of all letters, the winning layout is:
    
    B Y O U  L D W V Z
    C I E A  H T S N Q
    G X J K  R M F P    
-->
    
We ran tests on the winning layout:
    
    1. Evaluate optimized layouts using interkey speed estimates   
    2. Evaluate variants of the candidate winner using interkey speed estimates
    3. Test sensitivity of the candidate winner to the scoring parameters

For test 1, we rescored all of the 20 top-scoring layouts optimized from the 20 initialized layouts, and replaced the factor matrix with the inter-key speed matrix. The same two layouts that tied for first place do so again. 

For test 2, we rescored all of the 5,040 variants of the candidate winner that were tied for first place, replacing the factor matrix with the interkey speed matrix. The candidate winner scored highest.

For test 3, we ran a test on the variants of the candidate winner layout to see how robust they are to removal of scoring parameters. We removed each of the 11 scoring parameters one by one and ranked the new scores for the variants. The candidate winner scored highest for 8 of the 11 cases, and second highest for two other cases, demonstrating that this layout is not sensitive to individual parameters.

### Step 5. Arrange non-letter characters in easy-to-remember places

Now that we have all 26 letters accounted for, we turn our attention to non-letter characters, taking into account frequency of punctuation and ease of recall.
    
### Frequency of punctuation marks

  - Statistical values of punctuation frequency in 20 English-speaking countries (Table 1): <br>
Sun, Kun & Wang, Rong. (2018). Frequency Distributions of Punctuation Marks in English: Evidence from Large-scale Corpora. English Today. 10.1017/S0266078418000512. <br> 
https://www.researchgate.net/publication/328512136_Frequency_Distributions_of_Punctuation_Marks_in_English_Evidence_from_Large-scale_Corpora
  <br>"frequency of punctuation marks attested for twenty English-speaking countries and regions... The data were acquired through GloWbE."
  "The corpus of GloWbE (2013) is a large English corpus collecting international English from the internet, containing about 1.9 billion words of text from twenty different countries. For further information on the corpora used, see https://corpus.byu.edu/."
  
  - Google N-grams and Twitter analysis: <br>
"Punctuation Input on Touchscreen Keyboards: Analyzing Frequency of Use and Costs" <br>
S Malik, L Findlater - College Park: The Human-Computer Interaction Lab. 2013 <br>
https://www.cs.umd.edu/sites/default/files/scholarly_papers/Malik.pdf <br>
 "the Twitter corpora included substantially higher punctuation use than the Google corpus,  <br>
 comprising 7.5% of characters in the mobile tweets and 7.6% in desktop versus only 4.4%...  <br>
With the Google corpus,only 6 punctuation symbols (. -’ ( ) “) appeared more frequently than [q]"

  - "Frequencies for English Punctuation Marks" by Vivian Cook <br>
http://www.viviancook.uk/Punctuation/PunctFigs.htm  <br>
 "Based on a writing system corpus some 459 thousand words long.  <br> 
 This includes three novels of different types (276 thousand words),  <br>
 selections of articles from two newspapers (55 thousand), <br> 
one bureaucratic report (94 thousand), and assorted academic papers <br>
on language topics (34 thousand). More information is in <br>
Cook, V.J. (2013) ‘Standard punctuation and the punctuation of the street’ <br>
in M. Pawlak and L. Aronin (eds.), Essential Topics in Applied Linguistics and Multilingualism,  <br>
 Springer International Publishing Switzerland (2013), 267-290"

  - "A Statistical Study of Current Usage in Punctuation": <br>
Ruhlen, H., & Pressey, S. (1924). A Statistical Study of Current Usage in Punctuation. The English Journal, 13(5), 325-331. doi:10.2307/802253

  - "Computer Languages Character Frequency"
by Xah Lee.  <br>
Date: 2013-05-23. Last updated: 2020-06-29. <br>
http://xahlee.info/comp/computer_language_char_distribution.html <br>
NOTE: biased toward C (19.8%) and Py (18.5%), which have high use of "_".

Frequency: 

             Sun:     Malik:   Ruhlen:    Cook:            Xah:
              /1M   N-gram %   /10,000   /1,000       All%  JS%   Py%

    .    42840.02      1.151       535     65.3       6.6   9.4  10.3
    ,    44189.96                  556     61.6       5.8   8.9   7.5
    "                  2.284        44     26.7       3.9   1.6   6.2
    '     2980.35      0.200        40     24.3       4.4   4.0   8.6
    -     9529.78      0.217        21     15.3       4.1   1.9   3.0
    ()    4500.81      0.140         7                7.4   9.8   8.1
    ;     1355.22      0.096        22      3.2       3.8   8.6
    z                  0.09                   -         -
    :     3221.82      0.087        11      3.4       3.5   2.8   4.7
    ?     4154.78      0.032        14      5.6       0.3
    /                  0.019                          4.0   4.9   1.1
    !     2057.22      0.013         3      3.3       0.4
    _                  0.001                         11.0   2.9  10.5


### Add punctuation keys and number keys

We will assign the most frequent punctuation according to Sun, et al (2018) to the six keys in the middle two columns:  . , " ' - ? ; : () ! _

<!--

            B Y O U   '  "   L D W V Z
            C I E A   ,  .   H T S N Q
            G X J K   -  ?   R M F P

We will use the Shift key to group similar punctuation marks (separating and joining marks in the left middle column and closing marks in the right middle column):

            B Y O U  '(  ")  L D W V Z #$ @`
            C I E A  ,;  .:  H T S N Q
            G X J K  -_  ?!  R M F P
-->

**Separating marks (left)**: The comma separates text in lists; the semicolon can be used in place of the comma to separate items in a list (especially if these items contain commas); open parenthesis sets off an explanatory word, phrase, or sentence. 

**Joining marks (left)**: The apostrophe joins words as contractions; the hyphen joins words as compounds; the underscore joins words in cases where whitespace characters are not permitted (such as in variables or file names). 

**Closing marks (right)**: A sentence usually ends with a period, question mark, or exclamation mark. The colon ends one statement but precedes the following: an explanation, quotation, list, etc. Double quotes and close parenthesis closes a word, clause, or sentence separated by an open parenthesis.

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

The three remaining keys in many common keyboards (flanking the upper right hand corner Backspace key) are displaced in special keyboards, such as the Kinesis Advantage and Ergodox. For the top right key, we will assign the forward slash and backslash: / \\. For the remaining two keys, we will assign two symbols that in modern usage have significance in social media: the hash/pound sign and the "at sign". The hash or hashtag identifies digital content on a specific topic (the Shift key accesses the dollar sign). The "at sign" identifies a location or affiliation (such as in email addresses) and acts as a "handle" to identify users in popular social media platforms and online forums.

<!--

The resulting engram-es layout:

         [{ 1| 2= 3~ 4+  5<  6>  7^ 8& 9% 0* ]} /\
            bB yY oO uU  '(  ")  lL dD wW vV zZ #$ @`
            cC iI eE aA  ,;  .:  hH tT sS nN qQ
            gG xX jJ kK  -_  ?!  rR mM fF pP
-->