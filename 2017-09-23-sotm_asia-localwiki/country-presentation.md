This presentation was going to be delivered by Dongpo Deng, who is a long-time OSM user and is very active in the Taiwan community.  Unfortunately he couldn't come so I'm delivering this speech for him.

OpenStreetMap Taiwan community started around 2006.  At 2007 we only had the coast line on the map.  Most area is blank.  At 2014 we have pretty good data in the major cities.  The community currently uses Facebook group, mailing list, and slack for communication.

The mappers in Taiwan.

About local chapter.

Here are some highlights of community activities in Taiwan for the last year.

Some OSM projects in Taiwan.  Import local government data to OSM.

WaterGo is a project that I'm personally involved.  It is a project to show drinking water on a web map.  We also build a feature for the users to submit corrections or new water sources data directly in the map view.  So it is not only about using the map data, but also creating map data within the context of using it.

Data quality is a research oriented project conducted by Dongpo Deng and XXX in Taiwan.  It's main results currently is a comparison study about the "quality" of OSM road data in Taiwan against the government road data.  The "quality" is measured by Jaccard index, as you can see in the formula here.  Basically it splits the area of comparison into 1km by 1km squares, extract the road data from both database, add a buffer width of 10m to the roads, and compute a certain ratio of the buffered road on both datasets that are not overlapping, which are the differences between the two datasets.  What's especially revealing about this approach is when you apply it to quantitatively measure the improvements of quality over time.  In 2016 Mapbox did a massive work of improving road data on OSM in Taiwan.  So this research did a comparison of quality using the same method on the datasets before and after Mapbox's work.  The following slides will show their findings on different road types.  The blue bars are the quality of the data in 2014, and the red bars are of the data in 2017.  The vertical axis is the count of OSM ways.  The horizontal axis is the distribution of the Jaccard index, so the more portion of the bars are on the right hand side, the better the data quality.  As you can see for primary roads, there is a growth in higher-quality portion and a decrease in the lower-quality portion, showing the improvements.  Similar results for motorways.  Residential road data is improving, along with an overall increase because the volume of the data increased.
