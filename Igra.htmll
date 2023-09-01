html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Preskakanje Prepreka</title>
    <style>
        /* CSS stilizacija */
        body {
            background-color: #f0f0f0;
            margin: 0;
            overflow: hidden;
        }
        #igra {
            position: relative;
            width: 400px;
            height: 200px;
            background-color: #fff;
            margin: 100px auto;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }
        #lik {
            position: absolute;
            bottom: 0;
            left: 50px;
            width: 50px;
            height: 50px;
            background-color: #007BFF;
        }
        .prepreka {
            position: absolute;
            bottom: 0;
            width: 30px;
            height: 30px;
            background-color: #FF5733;
        }
    </style>
</head>
<body>
    <div id="igra">
        <div id="lik"></div>
    </div>

    <script>
        // JavaScript interakcija
        const igra = document.getElementById("igra");
        const lik = document.getElementById("lik");

        let skok = false;
        let visina = 0;

        igra.addEventListener("click", () => {
            if (!skok) {
                skok = true;
                let interval = setInterval(() => {
                    if (visina >= 100) {
                        clearInterval(interval);
                        let padanje = setInterval(() => {
                            if (visina <= 0) {
                                clearInterval(padanje);
                                skok = false;
                            } else {
                                visina -= 5;
                                lik.style.bottom = visina + "px";
                            }
                        }, 20);
                    } else {
                        visina += 5;
                        lik.style.bottom = visina + "px";
                    }
                }, 20);
            }
        });
    </script>
</body>
</html>
