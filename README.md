# Sacar-todas-las-combinaciones-posibles-entre-dos-fechas-PHP

Libreria:
https://pear.php.net/package/Math_Combinatorics/

```php
$f1 = "2021-05-19";
    $f2 = "2021-05-31";

    $objDate = new \App\Lib\BreakDate($f1,$f2);

    $dates = $objDate->getDates();
    $c_dates = count($dates);

    $combinations  = array();
	$combinatorics = new \App\Lib\Math_Combinatorics();

	foreach (range(1, $c_dates) as $number_of_combinations) {
	    foreach ($combinatorics->combinations($dates, $number_of_combinations) as $combination) {
	        $combinations[] = $combination;
	    }
	}

	dd($combinations);
```
