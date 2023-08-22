/* database */
<?php
    $db = mysqli_connect("localhost","root","","pass");
?>
/* posting */
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
    <form action="validation.php" method="post">
      <div>
        <input type="text" name="text" id="">
      </div>
      <div>
        <input type="text" name="flexing" id="">
      </div>
      <div>
        <input type="submit" value="submit" name="submit">
      </div>
    </form>
</body>
</html>
/* posting */
<?php
    include "connect.php";

    $sql = "SELECT * FROM send";

    $mysqli = mysqli_query($db, $sql);
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Apelyedo</th>
            </tr>
        </thead>
        <tbody>
            <?php while ($connect = mysqli_fetch_array($mysqli)) {?>
            <tr>
                <th><?php echo $connect["name"];?></th>
                <th><?php echo $connect["passage"];?></th>
            </tr>
            <?php } ?>
        </tbody>
    </table>
</body>
/* validation */
<?php
    include "connect.php";

    $sql = "SELECT * FROM send";

    $mysqli = mysqli_query($db, $sql);
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Apelyedo</th>
            </tr>
        </thead>
        <tbody>
            <?php while ($connect = mysqli_fetch_array($mysqli)) {?>
            <tr>
                <th><?php echo $connect["name"];?></th>
                <th><?php echo $connect["passage"];?></th>
            </tr>
            <?php } ?>
        </tbody>
    </table>
</body>
</html>
</html>
