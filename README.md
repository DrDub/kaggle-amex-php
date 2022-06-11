# American Express - Default Prediction Kaggle Competition - Rubix PoC

This project contains submissions for the [American Express - Default Prediction Kaggle competition](https://www.kaggle.com/competitions/amex-default-prediction) using PHP [RubixML](https://rubixml.com/). Some of the scripts ar  [static-notebooks](https://github.com/DrDub/static-notebook).

## Requirements

PHP extension [igbinary](https://www.php.net/manual/en/book.igbinary.php) needs to be installed.

```bash
composer require rubix/ml
composer require abbadon1334/gnuplot "dev-master"
kaggle competitions download -c amex-default-prediction
mkdir data
cd data
unzip ../amex-default-prediction.zip
cd ..
mkdir work
```
# Submission 1

```bash
php -d process-data.php
```

Creates ```work/training-data.bin```.

```bash
php -d submit1.php
```

Creates ```work/submit1.model```.

```
php -d submit1-apply.php
```

Creates ```work/submission1.csv```.

[Upload](https://www.kaggle.com/competitions/amex-default-prediction/submit) to Kaggle the file ```work/submission1.csv```

