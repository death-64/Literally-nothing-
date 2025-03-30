<!DOCTYPE html><html>
<head>
    <title>Hey, I wanna ask you something</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            overflow: hidden;
            background-color: ;
            color: black;
        }.rainbow-text {
        font-size: 40px;
        font-weight: bold;
        animation: rainbow 20s infinite;
    }

    @keyframes rainbow {
        0% { color: red; }
        20% { color: orange; }
        40% { color: yellow; }
        60% { color: green; }
        80% { color: blue; }
        100% { color: purple; }
    }

    .glitch-text {
        font-size: 40px;
        font-weight: bold;
        color: red;
        animation: glitch 0.0002s infinite;
    }

    @keyframes glitch {
        0% { transform: translate(20px, -200px) rotate(3601deg); }
        20% { transform: translate(-200px, 200px) rotate(-3601deg); }
        40% { transform: translate(30l0px, -300px) rotate(3600deg); }
        60% { transform: translate(-100px, 30px) rotate(-3600deg); }
        80% { transform: translate(20px, -20px) rotate(3600deg); }
        100% { transform: translate(50, 90) rotate(3600deg); }
    }

    .fire-text {
        font-size: 40px;
        font-weight: bold;
        color: orange;
        animation: fire 015s infinite alternate;
    }

    @keyframes fire {
        0% { text-shadow: 0px 0px 5px orange, 0px 0px 10px red; }
        50% { text-shadow: 0px 0px 10px yellow, 0px 0px 20px orange; }
        100% { text-shadow: 0px 0px 5px orange, 0px 0px 10px red; }
    }

    .floating-text {
        font-size: 30px;
        color: black;
        animation: float 20s infinite ease-in-out;
    }

    @keyframes float {
        0% { transform: translateY(0px); }
        50% { transform: translateY(-10px); }
        100% { transform: translateY(0px); }
    }

    .spinning-button:hover {
        animation: spin 0.001s infinite linear;
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }

    @keyframes fall {
        0% { transform: translateY(0px); }
        100% { transform: translateY(100vh); }
    }
</style>

</head>
<body>
    <h1 class="rainbow-text">the one real important question</h1>
    <h1 class="glitch-text">u r so hot.a fan for u</h1>
    <h1 class="fire-text">🔥  </h1>
    <p class="floating-text">did u stopped eating shit??</p><form onsubmit="showMessage(event)">
    <input type="text" id="userInput" placeholder="Tell me">
    <button class="spinning-button" type="submit">submit</button>
</form>

<p id="outputMessage"></p>
<button id="throwShit">I've got ur leaked photo"press here" to see</button>

<script>
    function showMessage(event) {
        event.preventDefault();
        let userResponse = document.getElementById("userInput").value.trim().toLowerCase();
        let output = document.getElementById("outputMessage");
        if (userResponse === "yes") {
            output.textContent = "I always had a doubt on u cause u smelled really bad all the time!";
            output.style.color = "green";
        } else if (userResponse === "no") {
            output.textContent = "Still not? Had a doubt on u since childhood. Shame on u bruh!";
            output.style.color = "red";
        } else {
            output.textContent = "U fucking kidding me? Write YES or NO, u asshole!";
            output.style.color = "blue";
        }
    }

    document.getElementById("throwShit").addEventListener("click", function() {
        let shit = document.createElement("div");
        shit.innerHTML = "💩";
        shit.style.position = "absolute";
        shit.style.fontSize = "40px";
        shit.style.top = "-50px";
        shit.style.left = Math.random() * window.innerWidth + "px";
        shit.style.animation = "fall 3s linear forwards";
        document.body.appendChild(shit);
        setTimeout(() => { shit.remove(); }, 3000);
    });

    let text = "thanks for cumming...";
    let i = 0;
    function typeWriter() {
        if (i < text.length) {
            document.getElementById("outputMessage").innerHTML += text.charAt(i);
            i++;
            setTimeout(typeWriter, 100);
        }
    }
    window.onload = typeWriter;
</script>

</body>
</html>
