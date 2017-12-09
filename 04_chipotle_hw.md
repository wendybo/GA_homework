#### Look at the head and the tail of chipotle.tsv in the data subdirectory of this repo. 
$ git clone https://github.com/ga-students/DS-SEA-08.git  
$ cd DS-SEA-08/  
$ cd data  
$ head chipotle.tsv  
order_id        quantity        item_name       choice_description      item_price
1       1       Chips and Fresh Tomato Salsa    NULL    $2.39
1       1       Izze    [Clementine]    $3.39
1       1       Nantucket Nectar        [Apple] $3.39
1       1       Chips and Tomatillo-Green Chili Salsa   NULL    $2.39
2       2       Chicken Bowl    [Tomatillo-Red Chili Salsa (Hot), [Black Beans, Rice, Cheese, Sour Cream]]      $16.98
3       1       Chicken Bowl    [Fresh Tomato Salsa (Mild), [Rice, Cheese, Sour Cream, Guacamole, Lettuce]]     $10.98
3       1       Side of Chips   NULL    $1.69
4       1       Steak Burrito   [Tomatillo Red Chili Salsa, [Fajita Vegetables, Black Beans, Pinto Beans, Cheese, Sour Cream, Guacamole, Lettuce]]      $11.75
4       1       Steak Soft Tacos        [Tomatillo Green Chili Salsa, [Pinto Beans, Cheese, Sour Cream, Lettuce]]       $9.25  

$ tail chipotle.tsv  
1831    1       Carnitas Bowl   [Fresh Tomato Salsa, [Fajita Vegetables, Rice, Black Beans, Cheese, Sour Cream, Lettuce]]  $9.25
1831    1       Chips   NULL    $2.15
1831    1       Bottled Water   NULL    $1.50
1832    1       Chicken Soft Tacos      [Fresh Tomato Salsa, [Rice, Cheese, Sour Cream]]  $8.75
1832    1       Chips and Guacamole     NULL    $4.45
1833    1       Steak Burrito   [Fresh Tomato Salsa, [Rice, Black Beans, Sour Cream, Cheese, Lettuce, Guacamole]]  $11.75
1833    1       Steak Burrito   [Fresh Tomato Salsa, [Rice, Sour Cream, Cheese, Lettuce, Guacamole]]       $11.75
1834    1       Chicken Salad Bowl      [Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Guacamole, Lettuce]] $11.25
1834    1       Chicken Salad Bowl      [Fresh Tomato Salsa, [Fajita Vegetables, Lettuce]]$8.75
1834    1       Chicken Salad Bowl      [Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Lettuce]]    $8.75  

#### What do you think each column means?  
The columns describe the components of an order including the order ID, the # of items in the order, the item name, the item description and the item price.  
#### What do you think each row means?  
Each row appears to be a component of an order since multiple orders have the same order ID number.  
#### How many orders do there appear to be?  
1834 orders

#### How many lines are in this file?  
4623  
$ wc -l chipotle.tsv
4623 chipotle.tsv

#### Which burrito is more popular, steak or chicken? chicken
$ grep "Steak Burrito" chipotle.tsv | wc -l
368
$ grep "Chicken Burrito" chipotle.tsv | wc -l
553

#### Do chicken burritos more often have black beans or pinto beans? Black Beans
$ grep "Chicken Burrito" chipotle.tsv | grep "Black Beans" | wc -l
282
$ grep "Chicken Burrito" chipotle.tsv | grep "Pinto Beans" | wc -l
105

#### Make a list of all of the CSV or TSV files in [our class repo] (https://github.com/ga-students/DS-SEA-08). (using a single command). 
$ find . -type f \( -name "*.tsv" -o -name "*.csv" \) | wc -l
30
$ find . -type f \( -name "*.tsv" -o -name "*.csv" \) -print
./data/airlines.csv
./data/Airline_on_time_west_coast.csv
./data/bank-additional.csv
./data/bikeshare.csv
./data/chipotle.tsv
./data/citibike_feb2014.csv
./data/cut_chipotle.tsv
./data/drinks.csv
./data/drones.csv
./data/hitters.csv
./data/icecream.csv
./data/imdb_1000.csv
./data/mtcars.csv
./data/NBA_players_2015.csv
./data/ozone.csv
./data/pronto_cycle_share/2015_station_data.csv
./data/pronto_cycle_share/2015_trip_data.csv
./data/pronto_cycle_share/2015_weather_data.csv
./data/rossmann.csv
./data/rt_critics.csv
./data/sms.tsv
./data/stores.csv
./data/syria.csv
./data/time_series_train.csv
./data/titanic.csv
./data/ufo.csv
./data/vehicles_test.csv
./data/vehicles_train.csv
./data/yelp.csv
./notebooks/GMapJson.csv

#### Count the approximate number of occurrences of the word "dictionary" (regardless of case) across all files of [our class repo] (https://github.com/ga-students/DS-SEA-8).
$ grep -r "dictionary" . | wc -w
886
886 instances of the word "dictionary"
