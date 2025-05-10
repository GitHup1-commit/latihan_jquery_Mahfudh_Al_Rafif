<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Latihan jQuery Mahfudh</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #e0eafc, #cfdef3);
      text-align: center;
      padding: 50px;
    }
    h2 {
      margin-bottom: 30px;
    }
    .button-container {
      margin-bottom: 20px;
    }
    button {
      padding: 10px 15px;
      margin: 5px;
      border: none;
      border-radius: 8px;
      background-color: #333;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background-color: #555;
    }
    #box {
      width: 300px;
      margin: 20px auto;
      padding: 20px;
      background-color: #4CAF50;
      color: white;
      border-radius: 10px;
      display: none;
    }
  </style>
</head>
<body>

  <h2>Latihan jQuery</h2>

  <div class="button-container">
    <button id="showBtn">Show</button>
    <button id="hideBtn">Hide</button>
    <button id="toggleBtn">Toggle</button>
    <button id="fadeInBtn">Fade In</button>
    <button id="fadeOutBtn">Fade Out</button>
    <button id="fadeToggleBtn">Fade Toggle</button>
    <button id="fadeToBtn">Fade To 50%</button>
    <button id="slideDownBtn">Slide Down</button>
    <button id="slideUpBtn">Slide Up</button>
    <button id="slideToggleBtn">Slide Toggle</button>
    <button id="chainBtn">Chaining Effect</button>
    <button id="resetBtn">Reset</button>
  </div>

  <div id="box">
    <h3>Selamat Datang!</h3>
    <p>Ini adalah kotak yang menggunakan semua efek jQuery!</p>
  </div>

  <script>
    $(document).ready(function(){
      $("#showBtn").click(function(){
        $("#box").show(1000);
      });

      $("#hideBtn").click(function(){
        $("#box").hide(1000);
      });

      $("#toggleBtn").click(function(){
        $("#box").toggle(1000);
      });

      $("#fadeInBtn").click(function(){
        $("#box").fadeIn(1000);
      });

      $("#fadeOutBtn").click(function(){
        $("#box").fadeOut(1000);
      });

      $("#fadeToggleBtn").click(function(){
        $("#box").fadeToggle(1000);
      });

      $("#fadeToBtn").click(function(){
        $("#box").fadeTo(1000, 0.5);
      });

      $("#slideDownBtn").click(function(){
        $("#box").slideDown(1000);
      });

      $("#slideUpBtn").click(function(){
        $("#box").slideUp(1000);
      });

      $("#slideToggleBtn").click(function(){
        $("#box").slideToggle(1000);
      });

      $("#chainBtn").click(function(){
        $("#box")
          .slideUp(800)
          .slideDown(800)
          .fadeTo(500, 0.6)
          .fadeTo(500, 1)
          .css({
            "background-color": "#ff9800",
            "border": "3px solid white",
            "box-shadow": "0px 0px 10px rgba(0,0,0,0.5)"
          })
          .animate({ fontSize: "20px" }, 500);
      });

      $("#resetBtn").click(function(){
        $("#box")
          .stop(true, true)
          .css({
            "background-color": "#4CAF50",
            "font-size": "16px",
            "box-shadow": "none",
            "border": "none"
          })
          .fadeIn(500)
          .fadeTo(500, 1);
      });
    });
  </script>

</body>
</html>
