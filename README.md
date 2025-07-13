# motivational-quotes
<?php
$quotes = [
    "The best way to get started is to quit talking and begin doing. – Walt Disney",
    "Don’t let yesterday take up too much of today. – Will Rogers",
    "It’s not whether you get knocked down, it’s whether you get up. – Vince Lombardi",
    "If you are working on something exciting, it will keep you motivated. – Steve Jobs",
    "Success is not in what you have, but who you are. – Bo Bennett",
    "The harder you work for something, the greater you’ll feel when you achieve it.",
    "Dream bigger. Do bigger.",
    "Don’t watch the clock; do what it does. Keep going. – Sam Levenson",
    "Great things never come from comfort zones.",
    "Push yourself, because no one else is going to do it for you."
];
$colors = [
    "#f7971e", "#ffd200", "#21d4fd", "#b721ff", "#43cea2", "#185a9d", "#f67280", "#c06c84"
];
$randomQuote = $quotes[array_rand($quotes)];
$randomColor = $colors[array_rand($colors)];
?>
<!DOCTYPE html>
<html>
<head>
    <title>Random Quote Generator</title>
    <style>
        body {
            background: linear-gradient(120deg, <?php echo $randomColor; ?>, #fff);
            min-height: 100vh;
            margin: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .quote-box {
            background: rgba(255,255,255,0.95);
            padding: 40px 50px;
            border-radius: 18px;
            box-shadow: 0 8px 32px rgba(33,212,253,0.18);
            max-width: 600px;
            text-align: center;
        }
        .quote {
            color: <?php echo $randomColor; ?>;
            font-size: 1.5em;
            font-style: italic;
            margin-bottom: 20px;
        }
        .refresh-btn {
            background: <?php echo $randomColor; ?>;
            color: #fff;
            border: none;
            padding: 12px 28px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1em;
            font-weight: bold;
            transition: background 0.3s;
        }
        .refresh-btn:hover {
            background: #222;
        }
    </style>
</head>
<body>
    <div class="quote-box">
        <div class="quote"><?php echo $randomQuote; ?></div>
        <form method="get">
            <button class="refresh-btn" type="submit">Show Another Quote</button>
        </form>
    </div>
</body>
</html>
