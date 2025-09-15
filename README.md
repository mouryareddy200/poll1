<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>User Favourite Actor Poll</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #6dd5ed, #2193b0);
      color: #fff;
      text-align: center;
      padding: 50px;
    }
    h1 {
      margin-bottom: 20px;
    }
    form {
      background: rgba(0,0,0,0.6);
      padding: 30px;
      border-radius: 15px;
      display: inline-block;
    }
    input, select, button {
      padding: 10px;
      margin: 10px;
      border-radius: 8px;
      border: none;
      font-size: 16px;
    }
    button {
      background-color: #ff9800;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background-color: #e68900;
    }
  </style>
</head>
<body>

  <h1>🎬 Favourite Actor Poll (India 2025)</h1>

  <form id="pollForm">
    <label for="username">Enter Your Name:</label><br>
    <input type="text" id="username" name="username" required><br><br>

    <label for="actor">Choose Your Favourite Actor:</label><br>
    <select id="actor" name="actor" required>
      <option value="">--Select Actor--</option>
      <option value="Shah Rukh Khan">Shah Rukh Khan</option>
      <option value="Salman Khan">Salman Khan</option>
      <option value="Aamir Khan">Aamir Khan</option>
      <option value="Prabhas">Prabhas</option>
      <option value="Allu Arjun">Allu Arjun</option>
      <option value="Ram Charan">Ram Charan</option>
      <option value="Mahesh Babu">Mahesh Babu</option>
      <option value="Rajinikanth">Rajinikanth</option>
      <option value="Vijay">Vijay</option>
      <option value="Dhanush">Dhanush</option>
      <option value="Yash">Yash</option>
      <option value="Mammootty">Mammootty</option>
      <option value="Mohanlal">Mohanlal</option>
      <option value="Ranbir Kapoor">Ranbir Kapoor</option>
      <option value="Ranveer Singh">Ranveer Singh</option>
      <option value="Vijay Deverakonda">Vijay Deverakonda</option>
      <option value="Sampoornesh Babu">Sampoornesh Babu</option>
      <option value="None of the Above">None of the Above</option>
    </select><br><br>

    <button type="submit">Submit</button>
  </form>

  <p id="result"></p>

  <!-- Background Music -->
  <audio id="bgm" loop>
    <source src="download10.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <script>
    // Handle form submission
    document.getElementById("pollForm").addEventListener("submit", function(event) {
      event.preventDefault();
      let name = document.getElementById("username").value;
      let actor = document.getElementById("actor").value;
      document.getElementById("result").innerHTML = 
        "🎉 Thank you <b>" + name + "</b>! Your favourite actor is <b>" + actor + "</b>.";
    });

    // Play BGM on first click anywhere
    document.body.addEventListener("click", function () {
      document.getElementById("bgm").play();
    }, { once: true });
  </script>

</body>
</html>
