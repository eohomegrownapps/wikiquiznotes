# WikiQuiz


## Basic description:

WikiQuiz is an educational game[1] which uses a Wikipedia topic[2] to create a
multiple choice test[3].

[1]: It's probably not going to be reliable enough to be used as a true
     'learning tool' e.g. revi.se, Anki/SuperMemo, so placing ourselves into
     the category of 'fun kinda educational things' in the vein of Oregon Trail
     gives us a lot of freedom to be creative rather than make it business-like
     while still appealing to the YRS idea of being actually somewhat useful
     (maybe :D)

[2]: 'topic' can include different words (articles) on the same topic, which is
     a sort of stretch goal for us.

[3]: Wikipedia mentions that questions aren't the only things in multiple
     choice tests (http://en.wikipedia.org/wiki/Multiple_choice#Examples)
     We could implement that idea later, perhaps.


## Detailed description

WikiQuiz is a educational game which tries to generate questions on a topic you
specify using a matching Wikipedia article. It utilises MediaWiki's API to
request articles based on a topic (Tues 30/07/14, currently only requests the
topic, but we hope to later add x-ility to find and use other relevant
articles), then parses the page and finds facts it can reliably understand,
which it then forms into questions using the simplenlg library. Each question
is presented with 3 answers, 1 being the correct one taken from the parsed
sentence and the other 2 being 'dud' answers, taken from either (!!) our list
of generic answers, or different sentences in the article.


## Program overview

The project is split into 3 main sections, each signifying an abstract **function?/idea?**.
The implementation is described in substeps.

    1. Prepare a MediaWiki article
        1.1 Retrieving a MediaWiki article in HTML/Wiki markup in a JSON
            container
        1.2 Parsing the JSON to get only the article content
    2. Analyse article
        2.1 Search for indicators of relevant (to the topic) statements
            2.1.1 Wiki markup """bold""" -- important
            2.1.2 Wiki markup [[link]] -- important
        2.2 Check whether there is a statement or fact which can be understood
            from the sentence
            2.2.1 Conjugations of the verb 'to be'
        2.3 (???) Set three variables: subject, verb, object (latter = meaning
            or description of the subject)
    3. Form question & multiple-choice answers
        3.1 Form the understood factoid into a question
