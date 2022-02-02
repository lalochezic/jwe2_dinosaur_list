# jwe2_dinosaur_list
**Disclaimer:**
I am well aware that the term *dinosaur* is reserved for land reptiles with their legs tucked underneath them and *do not* include marine or flying reptiles (pterasaurs). Jurassic World Evolution 2 doesn't make that distinction and neither do the players, but chill out; it's just a game.

## Hello Jurassic World
A list of dinosaurs players can collect from Jurassic World Evolution 2 (JWE2) formatted into a .csv. Data was collected and collated by [r/Reformater](https://www.reddit.com/user/Reformater/) and posted [here on Reddit](https://www.reddit.com/r/jurassicworldevo/comments/r30iz8/spreadsheet_detailing_how_to_unlock_every/). Their data has been made accessible [here](https://docs.google.com/spreadsheets/d/1TCE6igXMHr_OSvqULKU2dqDBft_v8goaqsdZXiC9xLU/edit?usp=sharing).

I simply downloaded the data and removed the columns containing the legends on the right and wrangled it to produce the data that you can access [here](https://raw.githubusercontent.com/lalochezic/jwe2_dinosaur_list/main/dino_list_Rfriendly.csv) or above. It is in a .csv file in long format, so it can be imported and manipulated in any data management or statistics software (e.g. R) to produce any kind of summary you want. Because it's in long format, you can save it as a .xlxs and put it through a pivot table to get summaries that way.

The [code](https://raw.githubusercontent.com/lalochezic/jwe2_dinosaur_list/main/dino_wrangling) is really just how I wrangled the data from wide to long format. I don't subscribe to either base R or tidyverse functions; with the way that I process work in my mind, I find functions from both usable and don't mind using things from either side. The code may be a bit ugly, but I know how to read it :P

Here's some data about the data:
## dino_wrangling
The code I used in R to wrangle the data.
| Package/Software | version |
|--------| ----------- |
| <code>R</code> | 3.6.3 |
| <code>stringr</code> | 1.4.0 |
| <code>reshape2</code> | 1.4.4 |
| <code>tidyr</code> | 1.1.3 |
| <code>plyr</code> | 1.8.6 |
| <code>dplyr</code> | 1.0.6 |

## dino_list_Rfriendly.csv
| Header | Description |
|--------| ----------- |
| <code>species</code> | The species of dinosaur |
| <code>game.mode</code> | The game mode that you can play JWE2 in. Either Campaign, Chaos Theory, or Challenge mode |
| <code>game</code> | The scenario within a given game mode (see below) |
| <code>node.loc1</code> & <code>node.loc2</code> | The location of the research node that you need to reach in order to unlock this dinosaur. Specific to the Game Mode and Scenario you are playing in. 0 = Animal is available in-game through capture or being delivered; the prefix E indicates the dinosaur can only be unlocked on easy difficulty|

## legend_processed.csv
The legend for the [original dataset](https://docs.google.com/spreadsheets/d/1TCE6igXMHr_OSvqULKU2dqDBft_v8goaqsdZXiC9xLU/edit?usp=sharing). Used to change the codes within the dinosaur list into their full names.

## Scenarios within Game Modes
| Header | Description |
|--------| ----------- |
| Campaign | Arizona, Washington State, Pennsylvania, Oregon, California |
| Chaos Theory | Jurassic Park, Lost World, Jurassic Park 3, Jurassic World, Fallen Kingdom |
| Challenge | Canada, Germany, United Kingdom, Northwest USA, Southwest USA |
