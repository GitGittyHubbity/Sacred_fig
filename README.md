# Sacred_fig
<param ve-config 
       title="Religion’s Living Roots: The Sacred Ficus religiosa"
       author="Foo Shi Wen"
       banner="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/Ficus_religiosa_-_Fruits.jpg/640px-Ficus_religiosa_-_Fruits.jpg"
       layout="vertical">
       
Of the over 800 species in the genera *Ficus*[^1] , *Ficus religiosa* is likely among the most famous. *F. religiosa*, commonly known as the sacred fig or the bodhi tree, is a fig native to the Indian subcontinent, east Himalaya, Myanmar, and Malayan region.  The epithet, religiosa, alludes to its significance to Hinduism and Buddhism, two major religions also originating from the Indian subcontinent.[^2] Though the name *Ficus religiosa* was first designated by Carl Linnaeus in 1753, the species was later given eight other scientific names by subsequent taxonomists. These include *Ficus peepul* and *Urostigma affine*.[^3]  Paralleling its nomenclative popularity in the scientific world, *F. religiosa* also bears over 150 known vernacular names.[^4][^5] Table 1. illustrates some of the names in the various languages spoken in India alone. Common names today include the bodhi tree, peepal tree and the *Ashvattha* tree.[^6]  This richness in vernacular names reflects the species’ cultural importance and rich history.

For reference, first open the [Juncture user guide](https://github.com/JSTOR-Labs/juncture/wiki/visual-essay-tags) in a new tab. Then, go ahead and enter your essay title in the "title" field above, and your name as you'd like it to appear in "author". For the banner image, you can pick anything you already have permissions to use. The image will be automatically scaled to fit the field (or you can crop/create an image 1200 by 400 pixels).

## This is a quick Markdown tutorial. Two hashes precede a heading. You can use these headings to divide sections of your essay.

*This makes things italics*. 

This is how you add a footnote. [^1]

[This is how you add a link](https://www.juncture-digital.org/KatherineMEnright/speciesstories/)

This is how you add a mouse-over information panel from Wiki data: <span eid="Q170662">Mangosteen</span>
You can find the wikidata IDs by searching for proper nouns [here](https://www.wikidata.org/wiki/Wikidata:Main_Page). The ID is the series of digits following the letter Q.

**There's no spell-check feature built in, so keep a careful eye out!**

## Adding Images
       
You can use the QID tag within a sentence. For example: The <span eid="Q170662">mangosteen</span> is a non-native fruit found in Singapore. This is the code you use to add an image. Make sure to **close the tag**. It starts with **<param ve-image** and ends with a closing **>**. Within these tags, you can add information to help the program locate and describe the image. **While these examples are images, we can also include textual sources (particularly primary sources) in the media viewer where appropriate.**
<param ve-image 
       url="https://iiif.wellcomecollection.org/image/V0044770/full/1338%2C/0/default.jpg"
       title="Mangosteen Photograph" 
       description="A mangosteen plant (Garcinia mangostana): fruiting branch and halved fruit. Photograph. Wellcome Collection.">
       
<span eid="Q271648">Marianne North</span> painted this painting of a 'Singapore monkey' amongst mangosteen fruits in 1875. You can also include "attribution" in the image information.
<param ve-image 
       url="https://d3d00swyhr67nd.cloudfront.net/w1200h1200/collection/LSW/RBGM/LSW_RBGM_MN_CD6_577-001.jpg"
       title="Flowers and Fruit of the Mangosteen, and a Singapore Monkey" 
       description="Held by Kew Gardens."
       attribution="Marianne North"
       license="CC BY-NC">
       
These are both examples of images added *from urls*. This is the preferred method. However, there might be some images you have to upload yourself. That's totally fine! Ideally, these files should be *as small as possible* and only .jpg or .png files will work. You should create a folder in your repository called "media" and upload the file there. Then, for the url, just copy and paste the item path: "media/{filename}.jpg". For more information on adding multiple images, comparisons, curtain sliders, and for how to zoom into particular sections of an image, check out the documentation [here](https://github.com/JSTOR-Labs/juncture/wiki/Visual-Essay-Image-Tag).
<param ve-image 
       url="media/victoria-crowned=pigeon.jpg"
       title="Victoria crowned pigeon"
       attribution="Katherine Enright">     
## Map

Mangosteens are found in Singapore. This takes a base map and sets the center to Singapore. The code after creates markers for different species, for instance, or to mark particular places on a map.
<param ve-map center="1.35, 103.9" zoom="11">
<param ve-map-marker
       url="https://leafletjs.com/examples/custom-icons/leaf-green.png"
       coords="1.3621, 103.8198"
       size="38, 95"
       iconAnchor="22, 94"
       shadowUrl="https://leafletjs.com/examples/custom-icons/leaf-shadow.png"
       shadowSize="50, 64">
<param ve-map-marker
url="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Pinz%C3%B3n_azul_de_Gran_Canaria_%28macho%29%2C_M._A._Pe%C3%B1a.jpg/220px-Pinz%C3%B3n_azul_de_Gran_Canaria_%28macho%29%2C_M._A._Pe%C3%B1a.jpg"
       coords="1.4126, 103.9577"
       size="129, 170"
       circle="true">
    
    
You can create custom regions just by drawing shapes (no coding needed) using [geojson.io](https://geojson.io/#map=2/0/20). Then you can download the shape file and add it to your juncture media file as a map layer. Let's imagine this is the distribution range of your species.

<param ve-map center="1.35, 103.9" zoom="2">
<param ve-map-layer geojson url="/media/demomap.geojson" title="Sample Distribution"> 

## Add a YouTube Video
You can take the id from the YouTube URL. You can also define the start time with start="0:20" (for instance).
<param ve-video id="5upF4rJUxC4" title="NYBG 2019 Corpse Flower Timelapse">

## Add a Timeline
This uses the [Knightlab platform](https://timeline.knightlab.com/). The back-end, for you to use, will just be a googlesheets (so it's user friendly!). Here's an example:
<param ve-knightlab-timeline source="1T9E8QZRT7ZFFmb55uLpJUSnELKuqSsXlLmNuVXvOC_I" timenav-position="bottom" hash-bookmark="false" initial-zoom="1" height="640">


## Multiple viewers

Multiple viewers may be defined for a single paragraph of text.  The first viewer defined is displayed as the default viewer.  
Others are selectable using icons displayed in the top right margin of the paragraph.
<param ve-image 
       url="https://iiif.wellcomecollection.org/image/V0044770/full/1338%2C/0/default.jpg"
       title="Mangosteen Photograph" 
       description="A mangosteen plant (Garcinia mangostana): fruiting branch and halved fruit. Photograph. Wellcome Collection.">
<param ve-map center="Q334" zoom="11" prefer-geojson>

# References

[^1]: Citation. Make sure you include the colon or this won't work!
