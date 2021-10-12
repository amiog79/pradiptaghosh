# 𝗪𝗘𝗕𝗦𝗜𝗧𝗘 𝗕𝗬:- PRADIPTA GHOSH
# pradiptaghosh
# durgapuja
# 𝗜 𝗔𝗠 𝗙𝗥𝗢𝗠 𝗕𝗢𝗟𝗣𝗨𝗥
# দূর্গা পূজার শুভেচ্ছা ও আন্তরিক অভিনন্দন সকলকে
# <!DOCTYPE html>  
<html>
  <head>
    <title>Clock</title>
  <h1 style="font-size:50px;text-align:center;background:blue;color:white;">REALTIME 100% ACCURATE TIMETABLE</h1>
  </head>
  <style>
    h1{
      color:white;
      background-color: green;
      text-align: center;
      font-size: 40px;
      transition: 1s;
      font-style: italic;
    }
    h1:hover{
      letter-spacing: 10px;
      background-color: red
    }

    div{
      color:white;
      background-color: green;
      text-align: center;
      font-size: 40px;
      transition: 1s;
      font-style: all;
    }
    div:hover{
      letter-spacing: 10px;
      background-color: red
    }

    section{
      color:white;
      background-color: green;
      text-align: center;
      font-size: 40px;
      transition: 1s;
      font-style: italic;
    }
    section:hover{
      letter-spacing: 10px;
      background-color: red
    }

    *{
      margin:0;
      padding:0;
    }
    div{
      position:absolute;
      width:600px;
      height:120px;
      margin:-50px -300px;
      text-align:center;
      background:red;
      top:50%;
      left:50%;
      color:white;
      font-size:100px;
      font-family:sans-serif;
      letter-spacing: 7px;
      text-shadow:3px 3px 5px black;

    }
    section{
      display:inline-block;
      position:relative;
      width:100px;
      margin:1px;
      box-shadow:5px 5px 5px rgba(0,0,0,0.5);
      background-image: -webkit-linear-gradient(rgba(255, 255, 255, .2) 90%, transparent 10%, transparent);
      background-size: 1px 10px;
    }

  </style>
  <script>
    window.onload = function(){
      var numbers = true;
      
      var checkZeros = function(time){
        if (time < 10){
          time = "0" + time;
        }
        return time;
      };
      window.animate = function(){
       // body...
        var date = new Date();
        var hours = date.getHours();
        var minutes = date.getMinutes();
        var seconds = date.getSeconds();
        var string = '';
    
        document.getElementsByTagName("body")[0].style.backgroundColor = "rgba(" + hours * 10 + ", " + minutes * 4 + ", " + seconds*4 + ", 0.4)";
        if(numbers){
          string = "<span>" + checkZeros(hours) + "</span>:<span>" + checkZeros(minutes) + "</span>:<span>" + checkZeros(seconds) + "</span>";
        }else{
          string = "<section style='height:" + hours * 10 + "px;'></section><section style='height:" + minutes * 5 + "px;'></section><section style='height:" + seconds * 5 + "px;'></section>";
        }
        document.getElementsByTagName("div")[0].innerHTML = string;
        setTimeout(window.animate, 50);
      };
      window.onclick = function(){
        numbers = numbers ? false : true;
      };
      window.animate();
    };

  </script>
  <body>
    <div></div>
  </body>
</html>
