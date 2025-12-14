# Handling-Forms-In-PHP-Activity

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Discriminant of a Quadratic Equation</title>
</head>
<body>
    <h1>Discriminant of a quadratic equation</h1>
    <form method="post" action="">
        <label>A: Value of a here</label><br>
        <input type="number" name="a" required><br><br>
        
        <label>B: Value of b here</label><br>
        <input type="number" name="b" required><br><br>
        
        <label>C: Value of c here</label><br>
        <input type="number" name="c" required><br><br>
        
        <input type="submit" value="Submit">
    </form>

    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        $a = floatval($_POST['a']);
        $b = floatval($_POST['b']);
        $c = floatval($_POST['c']);
        
        // Discriminant formula: b² - 4ac
        $discriminant = ($b * $b) - (4 * $a * $c);
        
        echo "<h2>Discriminant: $discriminant</h2>";
        echo "<p>Calculation: b² - 4ac = ($b)² - 4*($a)*($c) = " . ($b*$b) . " - " . (4*$a*$c) . " = $discriminant</p>";
    }
    ?>
</body>
</html>
