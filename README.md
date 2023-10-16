# Comprobador_DNI
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        // Array de lletras para calcular la lletra del DNI
        var lletres = ['T', 'R', 'W', 'A', 'G', 'M', 'Y', 'F', 'P', 'D', 'X', 'B', 'N', 'J', 'Z', 'S', 'Q', 'V', 'H', 'L', 'C', 'K', 'E', 'T'];

        // Solicitar a l'usuari el numero de DNI
        var numeroDNI = prompt("Por favor, ingresa tu numero de DNI (sin la letra):");

        // Convertir el numero de DNI a un numero sencer
        var numeroDNISencer = parseInt(numeroDNI);

        // Comprobar si el numero de DNI es valid
        if (numeroDNISencer >= 0 && numeroDNISencer <= 99999999) {
            // Calcular la lletra del DNI
            var reste = numeroDNISencer % 23;
            var lletraCalculada = lletres[reste];

            // Solicitar a l'usuari la letra del DNI
            var lletraUsuari = prompt("Per favor, ingresa la lletra del teu DNI (en mayúscules):");

            // Converteix la lletra de l'usuari a mayúscules per comparar
            lletraUsuari = letraUsuario.toUpperCase();

            // Comprobar si la lletra de l'usuari coincideix amb la calculada
            if (lletraUsuari === lletraCalculada) {
                console.log("El numero i la lletra del DNI son correctes.");
            } else {
                console.log("La lletra que has indicat no es correcta.");
            }
        } else {
            console.log("El numero de DNI proporcionat no es valid.");
        }
    </script>
</body>
</html>
