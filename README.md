`node ../index.js -m munich.mbtiles -s style_circle1.json -o munich_opt_style_circle1.mbtiles`
```
Process results
• Removed 1 features in level 2
• Removed 1 features in level 3
• Removed 1 features in level 4
• Removed layer munich from zoom levels 2, 3, 4
```
correct

`node ../index.js -m munich.mbtiles -s style_circle1.json -o munich_opt_style_circle1.mbtiles`

```
• Removed 1 features in level 0
• Removed 1 features in level 1
• Removed layer munich from zoom levels 0, 1
```
correct


`node ../index.js -m munich.mbtiles -s style.json -o munich_opt_style.mbtiles`

```
Process results
• Removed 1 features in level 0
• Removed 1 features in level 1
• Removed layer munich from zoom levels 0, 1
```
incorrect. Shouldn't remove anything because the layer gets used in all zoom levels