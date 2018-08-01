# Extractive sentence summarization

In this notebook I provide a python class for creating a full-sentence summary of document. Sentence summary is useful for document summary applications where it is beneficial to give users a quick sense of what is contained in the document to determine if they wanted to read further. There are two different categories of text summarization techniques: extractive and abstractive. Extractive techniques generally require less data, are unsupervised, and "extract" sentences from the document. Conversly, abstrative techniques require labeled training data, are supervised, and create summaries made up of generated, rather than extracted sentences. Methods, which are implemented in the open source package sumy, are all extractive and include KL-sum, Edmundson, LexRank, LSA, and random.

## Packages

Package versions are:

```
sumy==0.7.0
nltk==3.2.5
```

## Usage

To clone this notebook:

`git clone https://github.com/josiahdavis/extractive-sentence-summarization.git`


To run a simple example:

```
from nltk.corpus import stopwords
sw = stopwords.words('english')

se = SentencesExtractor(
    summarization_method='lexrank'
    , sentences_count=2
    , stop_words=sw
    )


txttxt  ==  ''''''
 Megaflaps are steep stratal panels that extend far up the sides ofMegafla 
diapirs or their equivalent welds. They have multiple-kilometer fold
widths and structural relief and  are thus distinct from smaller- scale
composite halokinetic sequences. Maximum dips range from near-vertical
to completely overturned. Although overturned megaflaps are associated with
flaring salt, there is no direct link between megaflap formation and the
initiation of salt sheets. Strata within a megaflap are usually convergent,
and the lower boundary is typically concordant with the top salt. The
upper boundary ranges between a prominent onlap surface and a more diffuse
zone of gradual rotation and thinning, and growth strata likewise display
both onlap and stacked wedge geometries. We use quantitative cross-section
restoration to elucidate the origin and development of megaflaps. Megaflaps
typically represent the relatively thin roofs of early salt structures that
include single- flap active diapirs, passive diapirs, salt pillows,
and salt sheets. They develop during halokinetic drape folding as the
minibasin sinks, during contractional squeezing of the diapir and its
roof, or during some combination of the two. The kinematics are dominated
by either limb rotation or kink-band migration, in which roof strata
move through a fold hinge into a lengthening steep megaflap. Both restoration
results and direct field evidence suggest that internal strain is minor,
with little bed lengthening and thinning. Recognition and understanding of
megaflaps are critical to successful petroleum exploration of three-way
truncation traps against salt. Megaflaps also have implications for the
lateral seal of stratigraphic traps and fluid pressures in minibasins
'''

result = se.extract(txt)

print('Document in {} sentences using {}:\n\n{}'.format(
    result['sentences_count'], 
    result['summarization_method'], 
    result['summary']))

```


