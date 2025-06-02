# cig-chinup-combo-chart (TBA)

SVG is 800 by 500 pixels, with 50 pixel buffer all around.

## Properties
- `cigData`: An array holding the values of the Line Chart.
- `chinupData`: An array holding the values of the Bar Chart.
- `maxUnits`: Maximum number of points on the y-axis to cater for.
- `dataPoints`: Maximum number of points on the x-axis to cater for.

## Methods
- `drawCharts()` :
  - Clear the SVG.
  - Call `drawAxes()`, passing in the SVG as an argument.
- `drawAxes(chart)`:
  - `chart` represents the SVG to populate.
  - Draw a vertical and horizontal line ofr the axes.
  - Define `pxPerUnit` as the number of pixels used for each vertical axis point.
  - Define `pxPerPoint` as the number of pixels used for each horizontal axis point.
  - Draw ticks on vertical axis using `pxPerUnit` as the spacing between each tick.
  - Draw ticks on horizontal axis using `pxPerPoint` as the spacing between each tick.
  - Call `drawLines()`, passing in the SVG as an argument, `pxPerUnit` and `pxPerPoint` as arguments.
  - Call `drawBars()`, passing in the SVG as an argument, `pxPerUnit` and `pxPerPoint` as arguments.
- `drawLines(chart, pxPerUnit, pxPerPoint)`:
  -  Use `pxPerUnit` and `pxPerPoint` to add line tags in `chart`.
  -  The data used is `cigData`.
- `drawBars(chart, pxPerUnit, pxPerPoint)`:
  -  Use `pxPerUnit` and `pxPerPoint` to add rect tags in `chart`.
  -  The data used is `chinupData`.
