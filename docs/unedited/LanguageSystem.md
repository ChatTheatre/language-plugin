%META:TOPICINFO{author=\"jamess\" date=\"1057356480\" format=\"1.0\"
version=\"1.9\"}% WebHome \| [Technical
Summaries](Builders.TechnicalSummaries) \| AccentSystem (Unimplemented)

# The Language System - A Technical Summary

Note: This document is currently under revision. See the S7 archives for
current information for now: \* May 12 -
<http://listserv.skotos.net/mailman/private/skotos-seven/2003-May/003351.html>
\* May 12 -
<http://listserv.skotos.net/mailman/private/skotos-seven/2003-May/003363.html>
\* May 19th first release in Merry -
<http://listserv.skotos.net/mailman/private/skotos-seven/2003-May/003424.html>
\* Also, the code of Zell:Actions on S7 contains information as well.

The rest of this is halfway through revision. \-- Main.JamesSanders - 04
Jul 2003

[]{.twiki-macro .TOC depth="4"}

## Language, the Basis of Culture

### It\'s Not What You Say, It\'s Whether They Understand It

Speech only conveys information between persons when they share a
language. There are many languages in the real world, and in most
simulated worlds. These different languages can be a barrier to
comprehension \-- this barrier can be a problem (when you want to make
yourself known to another person who does not know your language) or an
asset (when you want to hold what you assume is a private conversation
in a public place).

## Existing Approaches

Skotos.DartMUD has what our staff considers the best implemented
language system among existing MUDs and MUSHes. While our actual
phonetic system may be different, we don\'t expect vast differences
between our approach and that employed by Skotos.DartMUD.

In the Dragonrealms MUD, languages are handled in a strange and
unintuitive way. It is difficult to figure out how to actually speak a
\'foreign\' language in that game. Unknown languages get a sort of \'Bob
hisses and lisps in Dwarvish\' approach there.

## Problems Solved by Skotos Language System

An old dictionary defines language as \'the expression of thought in
words; the speech of one nation or race as distinguished from that of
another; style or expression peculiar to an individual, business or
science.\' Language is the major characteristic defining a race or
nation before modern times; as such, our language system will provide a
clear perception of this basic cultural difference to players.

The current system allows for the following: \*Easy understanding that
another language is being spoken, in a realistic presentation. \*Partial
comprehension of languages and resulting partial information transfer.
\*Realistic and gradual learning of new languages. \*Quick and intuitive
switching between language used.

Together these allow for realistic interactions between characters and
other characters, NPC\'s, and texts that use different languages with
varying skills.

## Summary of the Language System

### Listening to Foreign Languages

When hearing speech in a tongue completely unknown to his or her
character, the player will see a \'false language\' set of words, which
replace the words in the evoke.

As comprehension of the language increases, the number of \'false\'
words decreases, revealing the actual evoke beneath. The remaining
hidden words might be the longer ones in the evoke (is this feasible?).

At a certain level of comprehension, a player will stop seeing \"false
words\" and start seeing \"garbled words\" instead. He understands the
language and can guess at words without having to think about the
original alien words. This sets up a progression: \* No Skill: Character
only sees alien words \* Low Skill: Characters sees alien words and
simple words mixed \* Medium Skill: Characters see simple words and
garbles other words \* High Skill: Character understands everything

Our AccentSystem will allow players to activate an \'accent\' which
substitutes a few \'alien\' words or pronunciations into their evokes on
a consistent basis.

\<h3\>Speaking Various Languages\</h3\>

An imperfect speaker of some language will produce some \'garbled\' text
in his or her evokes using that language. Characters which understand
that tongue perfectly will still \'hear\' those garbles; characters with
little or no understanding of it will see a mixture of garble and
\'false language.\'

\<h3\>Written Text\</h3\>

When characters write or read text, the language system will produce
repeatable results; that is, when reading a document written in a
poorly-understood language, multiple readings should give the same (or
nearly the same) result.

\<h3\>Learning Languages\</h3\>

Gaining new languages should only be possible up to the limit imposed by
the language skill of an instructor. If the instructor has an accent in
the language being instructed, this should become available to the
student when speaking the new language.

------------------------------------------------------------------------

\<h2\>State of Development\</h2\>

Not currently implemented.

\<h3\>Open Issues in the Language System\</h3\>

\* switching between languages when speaking and writing.

\* How do we keep people from getting fed up with our language system
and just hopping over to IRC or one of chat rooms if they are trying to
speak with someone who doesn\'t understand their language?

\* what happens when people, upon hearing a consistent \'garble\', try
to respond with the \'consistent\' words they just heard.

\* *Example:* Sir Zell points to the beaver and says, \"Ge bloink,
bloink, zib flor ek bloink.\" You think, \"Ah, bloink must mean
\'beaver,\' and respond, \"Yah, that is the bloink.\" Shouldn\'t Sir
Zell hear you say, \"Gibber, gurble garble beaver.\"?

------------------------------------------------------------------------

------------------------------------------------------------------------

**TECHNICAL REQUIREMENTS:**

**Basic Requirements:** 1 Characters **Must** be able to know multiple
languages (see Builders.SkillSystem ) 2 Language **Must** be
comprehensible between two different people who both speak the lanaguage
3 Language **Must** be incomprehensible between two different people if
only one speaks the language 4 Language **May** be partially
incomprehensible if one or both people only partially understand a
language

So the basic idea is that there are languages, which probably act like
skills, and people can learn them. Language determines comprehension in
conversations.

**Picking Language Requirements:** 1 There **Must** be a global default
language, and default language difficulty. 2 Characters **May** be able
to set a default language to speak 3 Characters **Must** be able to
choose between languages to speak 4 Characters **May** be able to set a
language to use for a specific time duration, when talking to a specific
person, etc. 5 Characters **May** alter their language choice in the
evoke. 6 System **May** automatically choose appropriate languages

What language do you use every day? That\'s your default language, and
is probably the one you start with. A player should be able to change
his default language at a later time. A player should also be able to
choose the language he\'s using for a conversation or when speaking to a
specific person, etc. A really neat system would automatically select a
language to speak, based upon the context, who is being spoken to, and
what languages they seem to know.

**Writing Requirements:** 5 Writing and Speaking **Should** work
approximately the same 5 Writing **May** depend on a seperate skill,
which is itself dependent on the language skill 5 Speaking **May**
depend on a seperate skill, which is itself dependent on the language
skill

There may be some slight differences between writing and speaking,
mainly in that you can speak without writing, and to a lesser extent
write without speaking well, but for the most part the skills should be
the same.

**Garble Requirements:** 1 Proper names **May** not be garbled. 3
Characters **May** garble words/phrases/etc if their language skill is
low and they speak or write 5 Character **May** garble words/phrases/etc
if their language skill is low and they listen 4 Garbling **Must** occur
in a consistant manner for the same combination of speaker and listener
if the same phrase is used multiple times 4 Garbling **May** occur in a
different manner for each distinct speaker or listener

The GarbleSystem will define how garbling occurs, but the
Builders.LanguageSystem needs to define when it occurs. Words can get
garbled at two points: if a speaker says the wrong words and if a
listener hears the wrong words. A speaker should always say the same
wrong words and a listener should always hear the same wrong words.
However, different speakers may garble the same things in different ways
and different listeners may garble the same things in different ways.

It should be noted that this garbling involves translating words into
other words incorrectly, which might not be exactly what the garble
system does.

**Other Language Output Requirements:** 1 Listeners **Must** see
quasi-nonsense words which give an impression of the language if they
don\'t understand it at all. 2 Listeners **May** see quasi-nonsense
words interspaced with normal words if they only understand a language a
little bit.

If someone doesn\'t understand a language AT ALL then he should just see
words which give an impression of the language (Ork is a harsh language;
elfin is a soft language). This can be done by using word generation
tables. The original *Traveller* gives some excellent examples of how to
do this.

It\'s possible that we might want to mix these with understood words,
rather than doing a garble as described above, but this is probably only
appropriate at the lowest levels of skill. If we did this it would
probably be part of a continuum leading to the other garbling, described
above.

**Advanced Garble Requirements:** 1 **May** define words as simple or
complex 2 **May** translate into only simple words if speaker has a low
level of skill 3 **May** garble complex words if listener has a low
level of skill 4 the garbling **May** be affected by adverbs in the
evoke (i.e., loudly, slowly, clearly, carefully) 5 garbles **May** need
to be translated back (see open issues)

This is the \"bwa-ha-ha-soon-i-will-rule-the-world\" section of the
technical requirements. A very cool system would define the complexity
of words on a continuum and allow a speaker to say more complex words as
his skill increases and allow a listener to understand more complex
words as his skill increases.

This **may** actually be moderately easy to do by breaking words into
syllables and then use those syllables to define complexity. It\'s not a
totally accurate reflection, but it\'s a neat mechanistic way to do it.
Alternatively, a designer could sit down and design which words are
complex and which are simple in a specific language, which is more
realistic, but so much work that we probably shouldn\'t even consider
it.

**Language Tree Requirements:** 1 Some languages **May** default to
others for purpose of comprehension 2 Language trees **May** define
default comprehension

Languages trees are a very real concept. You can be understood in Italy
to a high level of comprehension if you speak Spanish. Likewise, you can
read some French if you speak Spanish. We can reflect this in Skotos\'
games by allowing languages to default to each other. A language tree
could outline all of this in a more complex yet consistant manner.

This may all be part of the Builders.SkillSystem .

------------------------------------------------------------------------

------------------------------------------------------------------------

References:

\* AccentSystem , SoundSystem , Builders.SkillSystem \* notes on
Skotos.DartMUDLanguage by Skotos.ChristopherAllen

------------------------------------------------------------------------

------------------------------------------------------------------------

More references

------------------------------------------------------------------------

------------------------------------------------------------------------

\<h1\>The Garble System - A Technical Summary\</h1\> see
TechnicalSummaries

See Also: GarbleNotes, AccentSystem , SoundSystem

------------------------------------------------------------------------

\<h2\>Try It Again, Loudly and Slowly\</h2\>

\<h3\>A Meaningful Sub-title for What Problems We trying to Solve\</h3\>

In a variety of cases, either due to inability to speak a language, or
due to ambient sound, information in speech can be lost.

\<h3\>Existing Approaches\</h3\>

DartMUD does this both in adjectives (what we call active markup) for
purposes of poorly written scrolls and signs, and for certain rooms like
waterfall rooms. What happens is that the garbled text is replaced with
appropriate histiogram text from the language that the player is
speaking (see Builders.LanguageSystem).

\<h3\>Problems Solved by the Garble System\</h3\>

Ok, there are many different problems that can be solved related to XYZ,
but these are the ones that we specifically are addressing in this
implementation of the XYZ System.

------------------------------------------------------------------------

\<h2\>Summary of the Garble System\</h2\>

This sentence should outline the definitions for major terms of art: \*
one \* two \* Etc.

\<h3\>First Definition\</h3\>

\<h3\>Second Definition\</h3\>

\<h3\>Etc.\</h3\>

------------------------------------------------------------------------

\<h2\>First major subsection, With a helpful title\</h2\>

There may only be one major subsection, describing the entire system.
More complex systems will be broken down into parts.

Describe how the System works in a variety of circumstances.

Start each major subsection off with a bulleted list on the major points
in the subsection: \* one \* two \* etc.

\<h3\>Minor Subsection\</h3\>

\<h3\>Minor Subsection\</h3\>

\<h3\>Minor Subsection\</h3\>

------------------------------------------------------------------------

\<h2\>Second major subsection, with a helpful title\</h2\>

etc.

Continue through all the major subsections of the system.

------------------------------------------------------------------------

\<h2\>State of Development\</h2\>

Not currently implemented.

\<h3\>Open Issues in the Garble System\</h3\>

\* A list of all of open issues.

------------------------------------------------------------------------

------------------------------------------------------------------------

**Area below not part of article, but just for notes and such when
we\'re putting the article together**

------------------------------------------------------------------------

------------------------------------------------------------------------

**TECHNICAL REQUIREMENTS:**

**General Requirements:** 1 **Must** decrease the comprehensibility of
evokes and \'written\' text

It\'s pretty easy to say **what** garble does in a general way. It makes
things harder to read. Exactly **how** that\'s done is a lot trickier.

**Incomprehensibility Requirements:** 1 **Must** garble words into
incomprehensibility 2 **Should** garble letters into incomprehensibility

One way to garble is to make things totally incomprehensible. It\'s not
very interesting, but it definitely get\'s the basic idea of garble
across.

This type of garble may still be useful for \"noise\" issues, though it
should be interspace with Near Thing Garble, moving over to
incomprehensibilty as the noise increases.

**Near Thing Requirements:** 1 **Should** garble words into similar
sounding words (speech) 2 written garbling **May** be garbled
differently from speech (evokes) 3 quiet and loud evokes **May** be
garbled differently 4 some garbles **Should** use the ellipsis rather
than deceptive phrasing.

This is the most likely type of garble when you\'re trying to comprehend
something. In writing, letters can get lost. Having arrays of letters
shapes would allow for transmuting letters in rational ways. Garbling
words into similar words could be useful in either speech or writing,
though the precise algorithms are different. Writing would be easier,
because you could search through a dictionary for words that look the
same and are of similar length. Similar sounding words would be a lot
easier, but you could cheat and just go with similar looking words
instead, after all we don\'t have voice chat.

This type of garble would be most useful for languages at medium levels
of skills. It would also be useful for \"noise\" issues if the noise
isn\'t too terribly bad.

**Language Requirements:** 1 **Should** garble words into another
language

This is described in more depth in the Builders.LanguageSystem . The
basic idea is that a method has been defined to describe the \"look and
feel\" of a language. If words can\'t be understood at all, they should
be garbled into the language using the defined method.

This type of garble would be most useful for languages at low or no
levels of skill.

**Advanced Requirements:** 1 **May** garble one syllable at a time

In noise situations, you could definitely hear only some of the
syllables of a few. Other syllables might be incomprehensible or
near-things. Language translations may also allow single syllable
translation, since you could understand a prefix or a suffix, but this
would be a lot harder to program in a sensical way.

------------------------------------------------------------------------

------------------------------------------------------------------------

References:

\* Other systems that impacts Garble:

\* Or systems Garble impacts: AccentSystem , SoundSystem ,
Builders.LanguageSystem

------------------------------------------------------------------------

------------------------------------------------------------------------

Put old text references here, between rulers.

------------------------------------------------------------------------

More references

------------------------------------------------------------------------

------------------------------------------------------------------------

\<H2\>Implementing Garble\</H2\>

I have been considering different ways to implement the Garble system,
and have decided on my first approach. The Garble system needs to be
implemented so that we can pass a garble function a sentence and get it
back with a percentage of the text having been translated into a
different language. For example:

        garble( "I really enjoy eating waffles on the porch.", 50, L_ELVISH );

might return:

        "I waith enjoy ian finwin on the porch."

in which roughly 50% of the language was translate into Elvish, using a
table of Elvish-sounding syllables.

If we want this process to be somewhat realistic, we need to ensure that
a word that is garbled in one sentence is always garbled everywhere for
people at that proficiency level. In other words, we can\'t just
randomly (even pseudo-randomly) replace half of the text with Elvish
syllables, because the player shouldn\'t understand \"waffles\" in one
sentence and not another. \"Waffles\" should always be translated as
\"finwin\" at a garble level of 50%. (This assumption is debatable, but
I am proceeding with it for now).

A simple approach would be to do the translation purely based on the
length of a word. For example, at 50% comprehension, a player
understands all words that are 6 letters long or less. While this would
work, it probably wouldn\'t take long for a player to realize what is
happening (\"Hey look, I always understand short words\"), which might
detract from that persons\' suspension of disbelief and enjoyment of the
game. We want to hide these sort of mechanics as much as possible from a
player.

The approach I\'m going to take is to give every word a summary value
based on the letter frequency value for each letter it contains. Letters
appear in the following frequency in English:

                     E T A I N O S H R D L U C M F W Y G P B V K Q J X Z

Using this, I will use a translation table that has values for each of
these letters as they are ordered above. I\'ll try a simple weighting
scheme at first (which might work out fine, or might need to be
fine-tuned), in which \"E\" will be worth 1 point, \"T\" worth 2 points,
etc. The word \"eat\", for example, would have a value of 1+3+2, or 6.
The word \"waffle\" would have a value of 16+3+15+15+11+1, or 61. Using
this approach, we can say that 50% comprehension equals an understanding
of all words with a total value of 55 or less (or whatever number proves
workable).

Also, we can use this total value to determine how many syllables a word
is to be replaced with, either using it as a seed or by defining some
general rules (every 30 points=1 syllable, etc). The seed idea might be
better, since there\'s no reason that a short word like \"dog\" would be
a short word in Elvish.

I like this approach because it is fast, duplicatable, and not easily
discernable to the player. It also takes into account that that longer
words tend to be harder to understand, and that less common letters have
some relationship to less frequent words. But the effects are somewhat
random and arbitrary, which should give it a more realistic feel.

\-- Skotos.EricOlsen - 26 May 2000 \<br\>

In a recent MUD-Dev post, an alternative way of representing which words
were foreign was interesting \"\"Blurh \[to the\] harken \[of the\]
jucieni, \[and once there\] areni buun lubadani.\" \-- ChristopherAllen

%META:TOPICMOVED{by=\"ChristopherAllen\" date=\"1057349976\"
from=\"Skotos.LanguageSystem\" to=\"Builders.LanguageSystem\"}%
