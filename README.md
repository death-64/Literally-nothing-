<!DOCTYPE html>
<html>
<head>
    <title>Hey, I wanna ask you something</title>
</head>
<body>
    <h1>koi aapse pyar kyu karega?</h1>
    <p>Just a random thought, don't mind that.<br> I just wanted to ask you <hr> did u stopped eating shit?</p>

    <form onsubmit="showMessage(event)">
        <input type="text" id="userInput" placeholder="Tell me">
        <button type="submit">don't press without typing anything</button>
    </form>

    
    <p id="outputMessage" style="font-weight: bold; color: blue;"></p>

    <script>
        function showMessage(event) {
            event.preventDefault(); // 

            let userResponse = document.getElementById("userInput").value.trim().toLowerCase();
            let output = document.getElementById("outputMessage");

            if (userResponse === "yes") {
                output.textContent = "i always had a doubt on u cause u smelled really bad all the time!";
                output.style.color = "green"; // Change text color
            } else if (userResponse === "no") {
                output.textContent = "still not, had a doubt on u since childhood shame on u bruh";
                output.style.color = "red";
            } else {
                output.textContent = "u fucking kidding me. write YES or NO  u asshole !";
                output.style.color = "blue";
            }
        }
    </script>
    
    
<p>tell me yes or no i wanna know from years tell me today</p>
</body>
</html>
