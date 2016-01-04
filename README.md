# ggforce
*Accelarating ggplot2*

[![Travis-CI Build Status](https://travis-ci.org/thomasp85/ggforce.svg?branch=master)](https://travis-ci.org/thomasp85/ggforce)

### About
ggforce is a package aimed at providing missing functionality to ggplot2 through
the extension system introduced with ggplot2 v2.0.0. In general ggplot2 has been
aimed primarily at ad hoc data visualization in order to investigate the data at 
hand, and less at utilities for composing custom plots a la D3.js. ggforce is 
mainly an attempt to address these "shortcomming" (design choices might be a 
better description). The long term goal is to have a repository of geoms, stats
etc that are as well documented and implemented as the official ones found in 
ggplot2.

#### Disclaimer
The inclusion of any geom, stat, position etc in ggforce is not necessarily a 
recommendation of their use. ggplot2 has been succesfull in being opinionated
about what functionality should be available. This is good as it insulates the
user from making bad decisions when analyzing their data, but it also makes it
difficult to develop novel visualizations using the ggplot2 API. ggforce on the
other hand positions itself closer to the "anything goes - the user is 
responsible for the quality of the output". Despite this keep in mind that some
things are always bad choices in data visualization: rainbow color scales, pie 
charts, overplotting etc. Don't do these things except with very good reasons.

### Current extensions
Following is a list of the functionality currently offered through ggforce

#### Geoms
- *geom_arc* Drawing of circle segments
- *geom_edge_bundle* Drawing of edge bundles from control points

#### Stats
- *stat_arc* Companion to geom_arc
- *stat_edge_bundle* Generate coordinates based on control points for use with
geom_edge_bundle

### Pending extensions
- scale_direction for symbolizing segment/path/line direction using a 
color/alpha gradient without occupying the color scale
- geom_spline for drawing xplines
- geom_arc_bar for drawing fat circle segments/wedges
- geom_circle for drawing circles based on coordinate system sizes
- geom_pie_point for drawing scatterplots based on small pie charts
- geom_wordcloud for drawing wordclouds
- position_steam for drawing steamgraphs
- stat_arc_stacked for automatically calculating data for pie/donut charts
- stat_path_dir and stat_segment_dir for calculating path and segments 
compatible with scale_direction
- trans_power for power transformations
- trans_radial for converting radial coordinates to cartesian
- reverse_trans for making a reverse transformation from any trans object

### Contributions
Pull and feature requests are very welcome. Obviously PR's will lead to faster
implementations than feature requests. I would like to urge requests to include
the following if possible:

#### Pull requests
If a PR is for a new feature, it should be self contained, possibly using 
already implemented functionality if applicable. All exported functions should
be documented following the style from ggplot2 using roxygen2 comment. You can
credit yourself with the implementation in the documentation. If the feature 
concerns a visualization appraoch invented by others, please link to the article
describing the approach.

#### Feature requests
If a feature is wished, but skill, time or other is lacking to create a full PR,
please file an issue. The feature request should provide a detailed description
of the nature of the feature, with links to relevant litterature describing the
visualization type, as well as possible use cases to guide in designing the use
cases.
