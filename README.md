# RadialGraph
A library for creating customisable, animated radial graphs for the use in your Android app.

This library aims to be a fully customisable radial graph to suit all your needs. If there is a feature you feel is
 missing or needs to be improved upon please reach out or feel free to contribute.
 
*Note:* This library only provisions for a radial graph composed of one or multiple head-to-tail stroked paths as
 shown Below:
 
 <img src="https://github.com/DuartBreedt/RadialGraph/blob/master/images/graph_example.png" width="320px" />

### Features
#### Graph
- Composed of `n` Sections
- Uses a data model to programmatically determine the graph's composition of Sections
- The graph stroke size can be set
- The colors of the Sections are customisable (see usage)
  - Gradients can also be applied for either the whole graph (FULL) or per section (SECTION)
- Customizable section caps
- A background Section track can be set for the graph as a solid color or bitmap image
- Graph Cap styles can be BUTT, ROUND, or SQUARE
- The graph end node can be set to ICON or PERCENT

#### Labels
- Toggleable labels
- By default the color is determined by the color of the Section which the label describes
- All label colors can be set globally for the graph
- Can display the value of the Section
- Can display the percent of the graph which the Section - that the label describes - comprises
- Can define custom text

#### Animation
- The graph has two main functions, `animateIn()` and `animateOut()`
- The direction of the animation can be defined as CLOCKWISE or COUNTERCLOCKWISE
- The animation duration can be specified in milliseconds

### Usage

#### 00 Dependency

```groovy
dependencies {
    implementation "com.duartbreedt.radialgraph:radialgraph:1.0.15"
}
```

#### 01 Layout

<img src="https://github.com/DuartBreedt/RadialGraph/blob/master/images/layout_example.png" width="320px" />

##### Note:
- If the `animationDuration` attribute is not specified then it will default to 1000ms.
- If the `animationDirection` attribute is not specified then it will default to `CLOCKWISE`.
- By default, labels are disabled.
- If the `labelsColor` attribute is not specified then it will default to the color of the section which it represents.
- If the `graphNode`/`fun setGraphNode(newGraphNodeType: GraphNode)` attribute is not specified then it will default to `NONE` and it won't display.
- If the `capStyle` attribute is not specified then it will default to the `BUTT`.
- If the `backgroundTrackColor`/`fun setBackgroundTrack(newColor: Int?)` or `backgroundTrackDrawable`/`fun setBackgroundTrack(newDrawable: Drawable?)` attribute is not specified then the background track will be disabled and not be rendered.
- Using a constraint dimension ratio of 1:1 is recommended for a scalable graph.
- Currently, if you are using labels you will need to set some padding to accommodate said labels.

#### 02 Config

<img src="https://github.com/DuartBreedt/RadialGraph/blob/master/images/config_example.png" width="320px" />

##### Note
- If the display mode is not specified for a section then it will display as a `DisplayMode.PERCENT` by default. 
- The Data object's second parameter is the total value of the graph. If it is not specified it is assumed that the sum of the sections comprise 100% of the graph.
- Note that a custom label - such as STAB - can be set for a specific section.

#### 03 Initialization

<img src="https://github.com/DuartBreedt/RadialGraph/blob/master/images/initialization_example.png" width="220px" />

#### 04 Animate In

<img src="https://github.com/DuartBreedt/RadialGraph/blob/master/images/animate_in_example.png" width="220px" />

### License
Copyright 2020 Duart Breedt

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

> http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
