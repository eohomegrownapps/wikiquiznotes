# Slides
1.                   WikiQuiz

say hello
group intro
project description
simple interface, lead on

"The interface [next slide] is Simple and Clean (Utada Hikaru):"


2.                 enter a word
       [image of the entry field with Vikings in]
       (dark grey) --> http://$lang.wikipedia.org/w/api.php?format=json&action=query&titles=$name&prop=revisions&rvprop=content)
                  ...receive quiz

only 1 field
+ optional language
use Wikipedia, == MediaWiki

"We ask the user for just one field: the topic they want to generate a quiz on.
You can also swap the 'language' between the normal English Wikipedia and the
Simple English Wikipedia. Using those two inputs, we request the Wikipedia page
that matches the topic.
We use Wikipedia's API, which is exposed by the wiki software that it runs on,
MediaWiki. This approach allows a great deal of flexibility in our game: as we
said, you can choose between 'simple' and 'normal' English Wikipedia, plus
because the game is able to request and parse data from any MediaWiki site, so
we could easily add an option to change which wiki site the user wants to
search."

what it is/does:
    - educational game
    - wikipedia article --> multiple choice test



3.        [image of sample question & answers

what the point is/reason for existence
Explanation of what it **appears** to do


3.               [[Wikipedia logo]]
                         =
                   [[MediaWiki]]

open data sources/data APIs (don't mention natural language)
Wikipedia - actually request page from MediaWiki, possible expansion
Data source = Wikipedia, but could later expand to other MediaWiki sites


4.      natural language:
            - English, not Python
            - Hard for machines to parse!


how we overcame 
        - Apache OpenNLP & simplenlg


5. x

tools - Java --> Eclipse --> Android SDK



6. Why we chose it

honest: not gonna be perfect
Oregon Trail - fun, kinda educational





9. End

Thanks Zach Holman (@holman) for his great resources on presenting and speaking.
