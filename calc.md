---
layout: default
title: Calculator
---

<html>

<html lang="en">
<head>
   <link rel="stylesheet" href="Calc.css">
   <title>Calulator</title>
</head>

<body>
   <div class="main">
      <input type="text" id = 'res'>
      <div class="btn">
         <input type="button" value = 'C' onclick = "Clear()">
         <input type="button" value = '%' onclick = "Solve('%')">
         <input type="button" value = '←' onclick ="Back('←')">
         <input type="button" value = '/' onclick = "Solve('/')">
         <br>
         <input type="button" value = '7' onclick = "Solve('7')">
         <input type="button" value = '8' onclick = "Solve('8')">
         <input type="button" value = '9' onclick = "Solve('9')">
         <input type="button" value = 'x' onclick = "Solve('*')">
         <br>
         <input type="button" value = '4' onclick = "Solve('4')">
         <input type="button" value = '5' onclick = "Solve('5')">
         <input type="button" value = '6' onclick = "Solve('6')">
         <input type="button" value = '-' onclick = "Solve('-')">
         <br>
         <input type="button" value = '1' onclick = "Solve('1')">
         <input type="button" value = '2' onclick = "Solve('2')">
         <input type="button" value = '3' onclick = "Solve('3')">
         <input type="button" value = '+' onclick = "Solve('+')">
         <br>
         <input type="button" value = '0' onclick = "Solve('0')">
         <input type="button" value = '.' onclick = "Solve('.')">
         <input type="button" value = '=' onclick = "Result()">
      </div>
   </div>
   <script src = 'calculator.js' ></script>
<style>
  body {
      background-color: #000000;
      color: #FF3131;
      animation: fadeInAnimation ease 3s;
      animation-iteration-count: 1;
      animation-fill-mode: forwards;
  }
  @keyframes fadeInAnimation {
      0% {
          opacity: 0;
      }
      100% {
          opacity: 0.75;
      }
  }
  h1::before {  
  transform: scaleX(0);
  transform-origin: bottom right;
}
h1:hover::before {
  transform: scaleX(1);
  transform-origin: bottom left;
}
h1::before {
  content: " ";
  display: block;
  position: absolute;
  top: 0; right: 0; bottom: 0; left: 0;
  inset: 0 0 0 0;
  background: rgb(0, 0, 0);
  z-index: -1;
  transition: transform .3s ease;
}
h1 {
  position: relative;
  color: rgb(0,255,255);
  font-size: 3rem;
  font-family: Monospace;
}
p {
  font-family: Monospace;
}
body {
  min-block-size: 100%;
  min-inline-size: 100%;
  margin: 0;
  box-sizing: border-box;
  display: grid;
  place-content: center;
  font-family: system-ui, sans-serif;
}
.block-container {
    padding-top: 1rem;
    padding-bottom: 0rem;
    padding-left: 5rem;
    padding-right: 5rem;
}
@media (orientation: landscape) {
  body {
    grid-auto-flow: column;
  }
}
</style>
</body>
</html>


</html>

