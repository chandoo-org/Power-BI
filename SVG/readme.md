# How to Create SVG Measures in Power BI with DAX

This repo has the files and necessary information about how to create SVG based DAX measures. For full article, refer to [SVG DAX Measures Tutorial](https://chandoo.org/wp/how-to-svg-dax-measures-power-bi/)

## Demo:

![SVG Measures in Power BI with DAX](https://github.com/chandoo-org/Power-BI/blob/c45a9e06e411beddafa4180e0dd172849581ac2f/SVG/svg-dax-measures-demo.gif)

## SVG Measure Code Template:

Use the below code to generate an SVG rectangle (bar chart) from your data.

```dax
SVG Rectangle = 
    var att_pct = [Attendance Percentage]
    var rect_width = 300 * att_pct
    var att_pct_disp = FORMAT(att_pct, "0%")
return
"data:image/svg+xml;utf8, 
<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 60'>
  <rect x='5.522' y='4.682' width='"&rect_width &"' height='50' style='fill:#DE913A; stroke: rgb(0, 0, 0);' rx='5.277' ry='5.277'/>
  <text style='fill: #111111; font-family: &quot;Arial&quot;, sans-serif; font-size: 28px; font-weight: 700; white-space: pre;' x='14.165' y='40.696'>"&att_pct_disp&"</text>
</svg>"
```

## Resources:

🧑‍💻 [Completed SVG Report PBIX](https://github.com/chandoo-org/Power-BI/blob/c45a9e06e411beddafa4180e0dd172849581ac2f/SVG/svg-examples-chandoo.pbix)

🔢 [Sample Data File](https://github.com/chandoo-org/Power-BI/blob/c45a9e06e411beddafa4180e0dd172849581ac2f/SVG/emp_attendance_data.xlsx)


📺 [Video Tutorial](https://www.youtube.com/watch?v=djUyi4oOAEM)

📃 [Blog Article](https://chandoo.org/wp/how-to-svg-dax-measures-power-bi/)

🗃️ [Ready to use SVG Templates](https://kerrykolosko.com/portfolio/)

🎨 [SVG Editor](https://boxy-svg.com/app)


