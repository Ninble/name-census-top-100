# Name Census top 100

The Name Census top 100 is a free name database with the 100 most common first names and the 100 most common surnames of 209 countries.
It is a sample of [Name Census](https://census.name), the name database with 7.983.828 first names and 11.986.282 surnames from 209 countries.
This edition was built in November 2026.

## Files

The database consists of four files, each available as CSV, JSON and SQL in UTF-8.

| File | Content | Rows |
|---|---|---|
| `first-name-database` | The top 100 first names of every country | 20.900 |
| `surname-database` | The top 100 surnames of every country | 20.900 |
| `first-name-countries` | One row per country with the population and how the first-name frequencies were obtained | 233 |
| `surname-countries` | The same for the surnames | 232 |

CSV files are separated by a semicolon.
JSON files hold an array of objects.
SQL files hold one `CREATE TABLE` and the `INSERT` statements.

## Columns

| Column | Description | Example |
|---|---|---|
| Name | The name as written in the country, in its own script | Сергей |
| Name ASCII | The name in plain letters a-z, empty for scripts without a plain form | sergey |
| Country code | ISO 3166-1 alpha-2 country code | RU |
| Country name | Name of the country | Russia |
| Continent | Continent of the country | Europe |
| Official | *y* when the name is on an official name list of the country, *n* when it is not | n |
| Gender | *m* or *f* for first names; for surnames the form (*m* or *f*, such as Иванов and Иванова), empty when both sexes use it | m |
| Unisex | *y* when a first name is used by both sexes (first names only) | n |
| Country Rank | Rank of the name in the country, 1 is the most common | 2 |
| Frequency | Number of people with the name in the country | 2467924 |
| Frequency source | *count* when the country publishes counts, *estimate* when the frequency is estimated | estimate |
| Quality | *ok* or *suspect* | ok |
| Script | Writing system of the name (ISO 15924) | Cyrl |
| Cumulative percentage | Share of the population with this name or a more common one | 3.836891 |

The countries files have the columns Country code, Country name, Continent, Population, Frequency source, Reliability and Usable profiles.

## Collection methodology

Our name database starts from official name lists published by governments and statistics offices.
3.512.525 first names and 4.134.135 surnames come from official lists of 52 countries.
Where a country publishes how many people have a name, we use that count.
Where it does not, we estimate the frequency from the share of the name among public Twitter profiles of the country and the population.
The column Frequency source tells which method was used for every name, and the countries files give the reliability per country.

The complete database with every name, and not only the top 100, is available on [census.name](https://census.name).
To split names into first name and surname, detect gender and nationality, use the [name parser API](https://parser.name).

## License

The Name Census top 100 is published under the GNU General Public License v3.0, see `LICENSE`.
