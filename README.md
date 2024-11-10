<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Koyfin Embeds</title>
    <style>
        body {
            background-color: cadetblue;
        }

        /* Basic container styling */
        .container {
            display: grid;
            gap: 3px;
            width: 100%;
            height: 100vh;
            padding: 3px;
            box-sizing: border-box;
            background-color: black;
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        /* Desktop layout: 2x2 grid */
        @media (min-width: 768px) {
            .container {
                grid-template-columns: 1fr 1fr;
                grid-template-rows: 1fr 1fr;
            }
            iframe {
                height: calc(50vh - 15px);
            }
        }

        /* Mobile layout: single column */
        @media (max-width: 767px) {
            .container {
                grid-template-columns: 1fr;
                grid-template-rows: auto;
                height: auto;
            }
            iframe {
                height: 60vh; /* Adjust height for better mobile view */
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Each iframe loads the Koyfin website -->
        <iframe width="650" height="450" src="https://embed.windy.com/embed.html?type=map&location=coordinates&metricRain=default&metricTemp=default&metricWind=default&zoom=5&overlay=radar&product=radar&level=surface&lat=30.501&lon=-87.879" frameborder="0"></iframe>
        <iframe src="https://globe.adsbexchange.com" allowfullscreen></iframe>
        <iframe width="650" height="450" src="https://embed.windy.com/embed.html?type=map&location=coordinates&metricRain=default&metricTemp=default&metricWind=default&zoom=5&overlay=wind&product=ecmwf&level=surface&lat=30.501&lon=-87.879" frameborder="0"></iframe>
        <iframe src="https://bamaone251.github.io/" allowfullscreen></iframe>
    </div>
</body>
</html>