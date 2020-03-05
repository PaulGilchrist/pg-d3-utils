# Commonly Used Utilities JavaScript Library

## Usage

```js
import d3Utils from 'd3-utils';
import 'd3-utils.css';
```

## Functions

`createBarGraph(el, tooltip, data, width, height, xKey, yKey, xToFixed, yToFixed, labels, warningLevel)`
`createLineChart(el, tooltip, data, width, height, xType, xKey, yKey, xToFixed, yToFixed, labels, warningLevel)` -Array must be sorted by x before passing to this function or the line will jump all over the place
`createPieChart(el, tooltip, data, width, xType, xKey, yKey, xToFixed, yToFixed, labels)`
`createScatterPlot(el, tooltip, data, width, height, xType, xKey, yKey, xToFixed, yToFixed, labels, warningLevel)` - Unlike LineChart, this array does not need to be sorted by x
`classPicker(value, warningLevel)`
`draw(type, el, tooltip, data, width, height, xType, xKey, yKey, xToFixed, yToFixed, labels, warningLevel)` - Set defaults for any properties not pased in
`getValue(inputValue, toFixed)`
`scale(data, xType, key, range, useMin = false)` - Scale to best fit data into viewable space
`showLabels(data, key, value, type, useMin = true)` - Allows for either showing no labels, just the min and max labels, or all labels

## Function Input Parameters

* `el` - the DOM element (usually a `<div>`) that the SVG will be appended to
* `tooltip` - The tooltip that should display when hovering over the chart.  Example:

```js
const tooltip = d3.select('body')
                .append('div')
                .attr('class', 'd3-utils-tooltip')
                .style('opacity', 0)
                .style('pointer-events', 'none')
                .style('position', 'absolute');
```

* `data` - Can be any complex object
* `xKey` - The `data` object's property used for the x-axis
* `yKey` - The `data` object's property used for the y-axis
* `xToFixed` - Level of precision when showing x value in tooltap.  Default=Infinity
* `yToFixed` -  Level of precision when showing y value in tooltap.  Default=Infinity
* `labels` - ?
* `warningLevel` - ?


