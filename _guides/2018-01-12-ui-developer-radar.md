---
layout: radar
title:  "UI Developer Radar"
date:   2018-01-12 09:33:37 -0500
description: UI Radar to help identify areas of improvement
lastUpdated: January 2018
trainings: [Angular,React,ES6,TypeScript,CSS Variables]
---

<script>
// Instructions:
//
// quadrant: 3, // 0,1,2,3 (counting clockwise, starting from bottom right)
// ring: 2,     // 0,1,2,3 (starting from inside)
// moved: -1    // -1 = moved out (triangle pointing down)
                //  0 = not moved (circle)
                //  1 = moved in  (triangle pointing up)

radar_visualization({
  svg_id: "radar",
  width: 1450,
  height: 1000,
  colors: {
    background: "#fff",
    grid: "#bbb",
    inactive: "#ddd"
  },
  quadrants: [
    { name: "Frameworks" },
    { name: "Tools" },
    { name: "Techniques" },
    { name: "Languages & Core APIs" }
  ],
  rings: [
    { name: "Essential",  color: "#93c47d" },
    { name: "Important", color: "#b7e1cd" },
    { name: "Nice to have",  color: "#fce8b2" },
    { name: "UI enthusiasts",  color: "#f4c7c3" }
  ],
  print_layout: true,
  entries: [
    // Frameworks
    { label: "AngularJS",   quadrant: 0, ring: 2, moved: -1 },
    { label: "Angular",     quadrant: 0, ring: 1, moved: 0 },
    { label: "ReactJS",     quadrant: 0, ring: 2, moved: 1 },
    { label: "Vue.js",      quadrant: 0, ring: 3, moved: 0 },
    { label: "Polymer",     quadrant: 0, ring: 3, moved: 0 },
    { label: "Bootstrap 4", quadrant: 0, ring: 2, moved: 1 },
    { label: "UI Kit",      quadrant: 0, ring: 3, moved: 1 },
    // Tools 
    { label: "Visual Studio Code",  quadrant: 1, ring: 2, moved: 1 },
    { label: "Webpack",             quadrant: 1, ring: 2, moved: 0 },
    { label: "Chrome Dev Tools ",   quadrant: 0, ring: 2, moved: 0 },
    { label: "ESLint",              quadrant: 1, ring: 2, moved: 0 },
    { label: "NPM",                 quadrant: 1, ring: 1, moved: 0 },
    { label: "Yarn",                quadrant: 1, ring: 2, moved: 1 },
    { label: "Sass",                quadrant: 1, ring: 1, moved: -1 },
    { label: "Less",                quadrant: 1, ring: 2, moved: -1 },
    // Techniques
    { label: "Assembling vs Crafting",  quadrant: 2, ring: 3, moved: 1 },
    { label: "API driven design",       quadrant: 2, ring: 3, moved: 1 },
    // Languages & Core APIs
    { label: "ES5",             quadrant: 3, ring: 0, moved: 0 },
    { label: "HTML",            quadrant: 3, ring: 0, moved: 0 },
    { label: "CSS 2",           quadrant: 3, ring: 0, moved: 0 },
    { label: "ES6",             quadrant: 3, ring: 1, moved: -1 },
    { label: "ES7",             quadrant: 3, ring: 3, moved: 1 },
    { label: "TypeScript",      quadrant: 3, ring: 1, moved: 1 },
    { label: "CSS 3",           quadrant: 3, ring: 2, moved: 1 },
    { label: "DOM API",         quadrant: 3, ring: 2, moved: -1 }
  ]
});

</script>
