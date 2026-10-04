
# CodeAlpha_Quote
<!DOCTYPE html>
<html>

<head>

    <title>Random Quote Generator</title>

    <style>

        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background: #f2f4f8;

            display: flex;
            justify-content: center;
            align-items: center;

            height: 100vh;
        }

        .container {
            width: 90%;
            max-width: 600px;

            background: white;

            padding: 40px 25px;

            border-radius: 15px;

            box-shadow: 0 5px 20px rgba(0,0,0,0.15);

            text-align: center;
        }

        h1 {
            margin-bottom: 30px;
        }

        #quote {
            font-size: 25px;
            font-style: italic;
            line-height: 1.5;

            margin-bottom: 20px;
        }

        #author {
            font-size: 18px;
            font-weight: bold;

            margin-bottom: 30px;
        }

        button {
            padding: 13px 25px;

            border: none;

            border-radius: 8px;

            background: #333;

            color: white;

            font-size: 16px;

            cursor: pointer;
        }

        button:hover {
            opacity: 0.8;
        }

    </style>

</head>


<body>

    <div class="container">

        <h1>💬 Random Quote Generator</h1>

        <div id="quote">
            "The best way to predict the future is to create it."
        </div>

        <div id="author">
            — Peter Drucker
        </div>

        <button onclick="newQuote()">
            New Quote
        </button>

    </div>


    <script>

        let quotes = [

            {
                text: "The best way to predict the future is to create it.",
                author: "Peter Drucker"
            },

            {
                text: "Success is not final, failure is not fatal.",
                author: "Winston Churchill"
            },

            {
                text: "Believe you can and you're halfway there.",
                author: "Theodore Roosevelt"
            },

            {
                text: "It always seems impossible until it's done.",
                author: "Nelson Mandela"
            },

            {
                text: "The secret of getting ahead is getting started.",
                author: "Mark Twain"
            },

            {
                text: "Dream big and dare to fail.",
                author: "Norman Vincent Peale"
            },

            {
                text: "Learning never exhausts the mind.",
                author: "Leonardo da Vinci"
            },

            {
                text: "Do something today that your future self will thank you for.",
                author: "Unknown"
            }

        ];


        function newQuote() {

            let randomNumber =
                Math.floor(Math.random() * quotes.length);


            document.getElementById("quote").innerText =
                '"' + quotes[randomNumber].text + '"';


            document.getElementById("author").innerText =
                "— " + quotes[randomNumber].author;

        }

    </script>

</body>

</html>