# jwe2_dinosaur_list
A list of dinosaurs players can collect from Jurassic World Evolution 2 (JWE2) formatted into a .csv. Data was collected and collated by [r/Reformater](https://www.reddit.com/user/Reformater/) in [their post on reddit](https://www.reddit.com/r/jurassicworldevo/comments/r30iz8/spreadsheet_detailing_how_to_unlock_every/). Their data has been made accessible [here](https://docs.google.com/spreadsheets/d/1TCE6igXMHr_OSvqULKU2dqDBft_v8goaqsdZXiC9xLU/edit?usp=sharing).

I simply downloaded the data and removed the columns containing the legends on the right and wrangled it to produce the data that you can access [here](https://raw.githubusercontent.com/lalochezic/jwe2_dinosaur_list/main/dino_list_Rfriendly.csv) or above. It is in a .csv file in long format, so it can be imported and manipulated to produce any kind of summary you want.

The [code](https://raw.githubusercontent.com/lalochezic/jwe2_dinosaur_list/main/dino_wrangling) is really just how I wrangled the data from wide to long format. I don't subscribe to either base R or tidyverse functions; with the way that I process work in my mind, I find functions from both usable and don't mind using things from either side. The code may be a bit ugly, but I know how to read it :P

Here's some data about the data:
## dino_wrangling
<code>R</code> version 3.6.3
  <p><code>stringr</code> version 1.4.0
  <p><code>reshape2</code> version 1.4.4
  <p><code>tidyr</code> version 1.1.3
  <p><code>plyr</code> version 1.8.6
  <p><code>dplyr</code> version 1.0.6

## dino_list_Rfriendly.csv
| Header | Description |
|--------| ----------- |
| species | The species of dinosaur |
| game.mode | The game mode that you can play JWE2 in. Either Campaign, Chaos Theory, or Challenge mode |
| game | The scenario within a given game mode (see below) |
| node.loc1 & node.loc2 | The location of the research node that you need to reach in order to unlock this dinosaur. Specific to the Game Mode and Scenario you are playing in. 0 = Animal is available in-game through capture or being delivered; the pre-fix E indicates the dinosaur can only be unlocked on easy difficulty|

## Scenarios within Games
| Header | Description |
|--------| ----------- |
| Campaign | Arizona, Washington State, Pennsylvania, Oregon, California |
| Chaos Theory | Jurassic Park, Lost World, Jurassic Park 3, Jurassic World, Fallen Kingdom |
| Challenge | Canada, Germany, United Kingdom, Northwest USA, Southwest USA |
