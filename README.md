# Report for Assignment 1

## Project chosen

Name: rpg_tactical_fantasy_game

URL: 

Number of lines of code and the tool used to count it: 12598 lines of code, counted using Lizard

Programming language: Python

## Coverage measurement

### Existing tool

We used Pytest (https://github.com/pytest-dev/pytest) and its coverage plugin _pytest_cov_, it was executed by Marcis
The tool was used to run the included tests from the _/tests_ ditectory with _pytest --cov=src/ --cov-report=html tests/_, this produced a code coverage of 58%:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Original%20Full%20Cov.jpg?raw=true)

### Your own coverage tool

#### Marcis
Animation.animate():

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/4e30744f16a57ab26969dfe5b207d7d4bf4eaedd

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Animation.animate%20Code.jpg?raw=true)

Coverage results for Animation.animate() by the instrumentation:

The instrumentation of the function produced a 75% branch coverage.

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Animation.animate%20branches.jpg?raw=true)

Shop.buy():

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/25857fe5ec0b5e33f3e3b68b8dff31e0fe7d0e95

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Shop.buy%20Code.jpg?raw=true)

Coverage results for Shop.buy() by the instrumentation:

After running the program(playing the game) a 100% branch coverage was achieved.

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Shop.buy%20branches.jpg?raw=true)

#### Nicolas
Movable.act():

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/239c7a62de721205426e51c7cee59f84a9274f60

(HAVE TO GET NEW SCREENSHOT!!)

Coverage results for Movable.act() by the instrumentation:

The instrumentation of the function produced a 80% (4/5) branch coverage.

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Movable.act%20branches.jpg?raw=true)

load_buildings():

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/8a1ac2fd767d56f285e873cebe08a4beadab000c

(HAVE TO GET NEW SCREENSHOT!!)

Coverage results for load_buildings() by the instrumentation:

The instrumentation of the function produced a 91% (10/11) branch coverage.

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Load_buildings%20branches.jpg?raw=true)

#### Stavroula
_process_next_animation_step():

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/07c88bbe0ca1c3f352e12f2197b0ab0e5145781c

(HAVE TO GET NEW SCREENSHOT!!)

Coverage results for _process_next_animation_step() by the instrumentation:

The instrumentation of the function produced a 100% branch coverage.

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/process_next_animation_step%20branches.jpg?raw=true)

_determine_players_initial_position():

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/285b011c6ffed9bdf20ab95728948c2814445f12

(HAVE TO GET NEW SCREENSHOT!!)

Coverage results for _determine_players_initial_position() by the instrumentation:

The instrumentation of the function produced a 75% (3/4) branch coverage.

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/determine_players_position%20branches.jpg?raw=true)

## Coverage improvement

### Individual tests

#### Marcis

test_animate.py:

Link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/17cb65ec5f95ff47d3023f0cf23f394f3bedbf45

Screenshots of the old and new coverage results for the function:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Function%20animate%20old%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Function%20animate%20new%20cov.jpg?raw=true)

Coverage improvement statement:

The new test was made to run the function multiple times to obtain the 75% branch coverage as was achieved during manual instrumentation, 
this resulted in a 73% code coverage, from the previous 0%, the missing 28% or 3 lines are in the branch that wasn’t reached during the test run.

test_shop.py:

Link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/86c4824144a33a95107f300c8b7ab006a1bf3fe3

Screenshots of the old and new coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Function%20buy%20old%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Function%20buy%20new%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20shop%20old%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20shop%20new%20cov.jpg?raw=true)

Coverage improvement statement:

Since a test for the shop feature of the program already existed, to add coverage for the Shop.buy() function, 
this test was enhanced by also calling this function with different parameters. This increased the function code 
coverage from 0% to 93% and increased the shop.py file code coverage from 49% to 70%.

#### Nicolas

movable.act.py:

Patch (diff) and link to commit with the instrumented code:

https://github.com/Grimmys/rpg_tactical_fantasy_game/commit/f403703fd27ddd09c42b5cd4beaf63eb315be1d8

(HAVE TO GET NEW SCREENSHOT!!)

Screenshots of the old coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/function%20act%20old%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20movable%20old%20cov.jpg?raw=true)

Screenshots of the new coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/function%20act%20new%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20movable%20new%20cov.jpg?raw=true)

Coverage improvement statement:

Since there was no previous coverage test for “act()”, the newly created test improved the function’s coverage from 0% to 83% (an 83% increase). 
The test also improved the overall coverage of the “movable.py” file from 73% to 80% (a 7% increase). The test was made to call the function several 
times with slightly different parameters, in order to reach as many branches as possible.

load_buildings.py:

Patch (diff) and link to commit with the instrumented code:

https://github.com/Grimmys/rpg_tactical_fantasy_game/commit/a9829085f8bb930bc60e70d92f4874cd434fb539

(HAVE TO GET NEW SCREENSHOT!!)

Screenshots of the old coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/function%20load_building%20old%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20tmx_manager%20old%20cov.jpg?raw=true)

Screenshots of the new coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/function%20load_building%20new%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20tmx_manager%20new%20cov.jpg?raw=true)

Coverage improvement statement:

Since there was no previous coverage test for “load_buildings()”, the newly created test improved the function’s coverage from 0% to 92% (an 92% increase). 
The test also improved the overall coverage of the “load_from_tmx_manager.py” file from 54% to 86% (a 32% increase). Since “load_buildings()” iterates through 
all buildings in the map, loading a level and calling the function executes most of the branches inside the function. At the end the test checks that the function 
executed and returned properly by checking that the array it returned is not empty.

#### Stavroula

test_fade_in_out_animation._process_next_animation.py:

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/50088ff98b837c8b2d3701ff5c502bc0d4118f14

(HAVE TO GET NEW SCREENSHOT!!)

Screenshot of the old coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/function%20process_next_animation_step%20old%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20fade_in_out%20old%20cov.jpg?raw=true)

Screenshot of the new coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/function%20process_next_animation_step%20new%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20fade_in_out%20new%20cov.jpg?raw=true)

Coverage improvement statement:

A new test had to be created for the previously instrumented function, which resulted in a coverage of 100%(a 100% increase). 
The test also improved the overall coverage of the “fade_in_out_animation.py” file from 0% to 78% (a 78% increase). 
This test was made to ensure that the fade in process and the fade out process correctly increment and decrement the opacity respectively.

test_level_utilitarian._determine_players_initial_position():

Patch (diff) and link to commit with the instrumented code:

https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/commit/7c0a06fbd39bcec9cef8fd86a8fea29d3cfc7501

(HAVE TO GET NEW SCREENSHOT!!)

Screenshot of the old coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20determine_players_initial_position%20old%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20level_scene%20old%20cov.jpg?raw=true)

Screenshot of the new coverage results for the function and the file:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20determine_players_initial_position%20new%20cov.jpg?raw=true)

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/file%20level_scene%20new%20cov.jpg?raw=true)

Coverage improvement statement:

The newly created test improved the function’s coverage from 0% to 80% (an 80% increase). The test also improved the overall coverage of the “level_scene.py” 
file from 38% to 41% (a 3% increase).This test searches for two people in the players list and checks if they have been assigned to a position.

### Overall

Old project coverage results:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Original%20Full%20Cov.jpg?raw=true)

New, improved project coverage results:

![alt text](https://github.com/CokeTree3/forkForSEP_rpg_tactical_fantasy_game/blob/master/doc_img/Final%20Full%20Cov.jpg?raw=true)

Coverage Statement:

The total coverage improved by 6%, from 58% to 64% of non-comment lines, though this also included the added code for function instrumentation 
which were not tested with the automated tests and so had a 0% coverage which reduced the overall improvement.


## Statement of individual contributions

#### Marcis:

- Instrumentation of functions Animations.animate() and Shop.buy()
- Code coverage improvement for testing, by creating tests for Animations.animate() and Shop.buy() functions
- General Python assistance
- Github branch merging
- Formatting of the “readme” file

#### Nicolas:

- Instrumentation and creation of the tests for function “movable.act()”
- Instrumentation and creation of the tests for function “load_buildings()”
- Formatting of the “readme” file
- Manual conversion of the "readme" file from text file to .md file using Github markdown

#### Stavrina:

- Instrumentation of the function “fade_in_out_animation._process_next_animation.py()” and creation of the test “test_fade_in_out_animation._process_next_animation.py”
- Instrumentation of the function “level_scene._determine_players_initial_position()” and creation of the test “test_level_utilitarian._determine_players_initial_position()”

