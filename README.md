## Test 1 ([style_circle1.json](https://github.com/indus/-vt-optimizer_issue13/blob/main/style_circle1.json))

`node ../index.js -m munich.mbtiles -s style_circle1.json -o munich_opt_style_circle1.mbtiles`
```
Process results
• Removed 1 features in level 2
• Removed 1 features in level 3
• Removed 1 features in level 4
• Removed layer munich from zoom levels 2, 3, 4
```
correct

## Test 2 ([style_circle2.json](https://github.com/indus/-vt-optimizer_issue13/blob/main/style_circle2.json))
`node ../index.js -m munich.mbtiles -s style_circle2.json -o munich_opt_style_circle2.mbtiles`

```
• Removed 1 features in level 0
• Removed 1 features in level 1
• Removed layer munich from zoom levels 0, 1
```
correct

## Test 3 ([style.json](https://github.com/indus/-vt-optimizer_issue13/blob/main/style.json))
`node ../index.js -m munich.mbtiles -s style.json -o munich_opt_style.mbtiles`

```
Process results
• Removed 1 features in level 0
• Removed 1 features in level 1
• Removed layer munich from zoom levels 0, 1
```
incorrect. Shouldn't remove anything because the layer gets used in all zoom levels.

It looks like the [last usage of the layer](https://github.com/indus/-vt-optimizer_issue13/blob/main/style.json#L23-L33) overwrites [previous usages](https://github.com/indus/-vt-optimizer_issue13/blob/main/style.json#L11-L22)