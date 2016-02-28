# Introduction #

The function of Text-To-Speech (TTS) system is to convert an arbitrary text to a spoken waveform. This
generally involves two steps

1. Text processing: converting the given text to sequence if synthesis units and

2.  Speech generation: generation of an acoustic wave form corresponding to each of these units
in the sequence.


# Features of Indian Language Scripts and Sounds: #
The scripts of Indian languages have originated from the ancient Brahmi script. The basic units of
writing system are characters which are orthographic representation of speech sounds. A character in
Indian language scripts is close to syllable and can be typically of the following form: C, V, CV, CCV
and CVC, where C is a consonant and V is a vowel. There are about 35 consonants and about 18 vowels
in Indian languages.
An important feature of Indian language scripts is their phonetic nature. There is more or less one to one
correspondence between what is written and what is spoken. The rules required to map the letters to
sounds of Indian languages are almost straight forward. All Indian language scripts have common
phonetic base.

## Letter to Sound Rules: ##
There is almost one to one correspondence between what is written and what is spoken in Indian
languages. This is the main logic this Text-To-Speech system lined in. For example the word “లండ􀃐”
(London) can be easily mapped to the sequence of consonants and vowel sounds as ల /ం/డ/ 􀃐
(la/on/da/n). This can be further split in to atomic units 􀃙/ A/ం/ 􀃉/A/ 􀃐. In Indian languages say
Telugu there are 11 vowels and 35 consonants.
Every consonant character is inherently bound with the vowel sound A, and is almost always
pronounced with this vowel gives a v-shaped head stroke to most of the Telugu letter, which is a
structural mark corresponding to the horizontal bar in Devanagari script and the arch in Oriya script.
When a virama (called viramamu in Telugu) or certain vowel characters are added to a consonant letter
A it is replaced. And if the inherited A is removed from consonant letter it bound with virama. As in
example డ is split to 􀃉 and A.
Similarly every constant character is mapped to its atomic virama form and vowel. So any character unit
can be split in to atomic units set “A - ః” and/or to set “॓ - 􀃘”. Now each atomic unit is mapped
corresponding recorded atomic unit sounds which are recorded in a quiet room with a noise canceling
microphone using the recording facilities of a typical multimedia computer system.


# Text Processing Front End: #
As we have discussed the issues related to text processing, let us briefly understand the nature of the text
for which synthesis systems are built.
## Format of Input Text: ##
The scripts of Indian languages are stored in digital computers in ISCII, UNICODE and in transliteration
schemes of various fonts. This TTS engine supports UNICODE format. However, the issue of various
formats could be conveniently separated from the synthesis engine.
As Indian languages have a common phonetic base, this engine is built for one transliteration scheme
and one language Telugu which can represent the scripts of all Indian languages.

## Mapping of Non-Standard Words to Standard Words and non-standard words: ##
In practice an input text such as news article consists of standard words such initials, digits, symbols and
abbreviations. Mapping of non-standard words to a set of standard words depends on the context, and it
is a non-trivial problem. For example, digit 120 has to expanded to /nuut`aa iravai/. “Rs 3005412” to
/muppia laqs-alaa aidu vela,nalagu van’dalaa pannen’d’u ruupayalu/, and etc can be mapped. Similarly
punctuation characters and their combinations such as :, < , >, !, % , which may be encountered in cases
of ratios, percentages, comparisons can be mapped to a set of standard words according to the context.


# Synthesis Approach: #
The text to be synthesized is analyzed and broken into sequence of atomic units to be selected and
concatenated in sound. The text that is given in UNICODE format is scanned one character after the
other and stored character array. Every consonant character scanned is inherently bound with the vowel
sound A as we discussed above. So the next character to consonant to be analyzed is identified. If the
identified character is consonant character then analyzing consonant character is broken to atomic units
as its viruma form and A. If the identified character is vowel then analyzing character is broken to
atomic units as its viruma form and identified vowel; instead of A.
All the atomic units are concatenated for every word and sound is produced using previously recorded
atomic units.


# Applications of Speech Synthesis Systems: #
The applications of speech synthesis systems are wide ranging including human-computer interaction,
telecommunications, talking books, language education and aid to handicapped persons.