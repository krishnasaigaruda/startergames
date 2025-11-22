

# Start html page


```
<!DOCTYPE html>
<html>
<head>
   <title></title>
</head>
<body>


</body>
</html> 
``` 

# example of the button in home to open screen
keeps the same styles just change file names.
```
<script>
    function openGame() {
      window.location.href = "Game1.html"; // Open in same tab
    }
  </script>

  <button onclick="openGame()" class="fancy-button">
    <div class="screen"></div>
    <div class="label">Tag game</div>
  </button>

```
# game page
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>game</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
    }

    .page-title {
      text-align: center;
      font-size: 32px;
      font-weight: bold;
      padding-top: 30px;
      color: #333;
    }

    .description {
      text-align: center;
      font-size: 16px;
      color: #555;
      padding: 10px 30px 40px;
      max-width: 800px;
      margin: 0 auto;
    }

    header {
      background-color: #333;
      padding: 20px 0;
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 10px;
    }

    button {
      background-color: #4CAF50;
      color: white;
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      cursor: pointer;
      border-radius: 6px;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #45a049;
    }

    .screen {
      display: none;
      padding: 40px;
      font-size: 24px;
      text-align: center;
    }

    .active {
      display: block;
    }

    .back-button {
      display: inline-block;
      background: linear-gradient(135deg, #0330f9 0%, #f34608 100%);
      color: white;
      text-decoration: none;
      padding: 12px 28px;
      font-size: 16px;
      font-weight: bold;
      border-radius: 25px;
      margin: 20px;
      box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
      transition: all 0.3s ease;
      border: 2px solid rgba(255, 255, 255, 0.2);
    }

    .back-button:hover {
      background: linear-gradient(135deg, #0084ff 0%, #ff9d00 100%);
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(102, 126, 234, 0.6);
    }

    .back-button:active {
      transform: translateY(0px);
      box-shadow: 0 2px 10px rgba(102, 126, 234, 0.4);
    }

    .back-button::before {
      content: "← ";
      font-size: 18px;
    }
  </style>
</head>
<body>
<a class="back-button" href="index.html">Back</a>

  <div class="page-title">game</div>

  <div class="description">
 ghjktyhjkl;thjk.
  </div>

  <header>
    <button onclick="showScreen('play')">Play</button>
    <button onclick="showScreen('download')">Download</button>
  </header>

  <div id="play" class="screen active">
 Lets play game
<iframe src="game3source.html" width="100%" height="800px"></iframe>
 <br/>
<br/>
<br/>
<br/>
<br/>
<h3>Game Controlls</h3>
<ul>
  <li>WASD Momement</li>
  <li>Arrow key can alo be used for movement</li>
</ul>
  </div>

  <div id="download" class="screen">
    Download Tag
    <div class="download-box">
        ⬇️ Click below to generate and download the file:
        <hr/>
        <h3>Steps to use</h3>
        <div style="text-align: left;">
      <ul>
            <li>Download</li>
            <li>Double click on the game1source.html.zip file</li>
            <li>when the game1source.html.zip file unzipps, double click on the
                game1source.html file that unzipps.
            </li>
            <li>Enjoy!</li>
        </ul>
    </div>
        <h3>If you are using in your website, pls give credit under game</h3>
        <br><br>
        <button class="download-link" onclick="downloadFile()">Download Game.html</button>
      

      </div>
      
      <style>
        .download-box {
          margin-top: 40px;
          text-align: center;
          font-size: 18px;
        }
      
        .download-link {
          background: linear-gradient(135deg, #2196F3, #1976D2);
          color: white;
          padding: 14px 26px;
          font-size: 18px;
          border: none;
          border-radius: 8px;
          cursor: pointer;
          transition: all 0.3s ease;
          box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
      
        .download-link:hover {
          background: linear-gradient(135deg, #1976D2, #0D47A1);
          transform: scale(1.05);
        }
      </style>
      
      <script>
        function downloadFile() {
         
      
          const link = document.createElement('a');
          link.href = "game1source.html.zip";
          link.download = 'Tag.html';
          document.body.appendChild(link);
          link.click();
          document.body.removeChild(link);
          URL.revokeObjectURL(url);
        }
      </script>
      

  <script>
    function showScreen(screenId) {
      document.querySelectorAll('.screen').forEach(screen => {
        screen.classList.remove('active');
      });
      document.getElementById(screenId).classList.add('active');
    }
  </script>

</body>
</html>
```
# IFRAME
```
<iframe src="game3source.html" width="100%" height="800px"></iframe>
```