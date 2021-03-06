# advent-of-code
Advent of Code is a series of small programming puzzles for a variety of skill levels. This contains both the [2016](https://adventofcode.com/2016) edition (done retroactively in JavaScript) and the [2018](https://adventofcode.com/2018) edition (done on time in JavaScript).

## Setup

- Clone the repository on your computer by running `git clone git@github.com:sebranly/advent-of-code.git` in a terminal
- You need to have `node` installed, my current version is `v8.9.0` (obtained after running `node --version`)
- Within the root repository in a terminal, run `npm install` (so that it creates the `node_modules` folder based on `package.json`)

## Execution

Within the root repository in a terminal, run `node index.js` after having hardcoded both the year and the day (and optional part in some cases for part 2) you want.

For example if you want to run day 9 of year 2018, go to `index.js` and change the two lines to:
```js
const DAY_NUMBER = 9; // This one
const YEAR = 2018; // This other one as well

const dayResult = solvers[YEAR][DAY_NUMBER - 1](daysInput[YEAR][DAY_NUMBER - 1]); // There is no need to change that one
```

### Note

As this repository is a work-in-progress and as my main focus for Advent of Code is solving challenges as fast as possible, the code I produce is most of the time not the most elegant one, although I spend time refactoring things before pushing it to GitHub.
For this reason, for some challenges, you might have to explicitly set the `partNumber` as well. For example if you see that the solution for `part2` of a problem doesn't appear or looks wrong, make sure to add the part within `index.js` in `const dayResult = solvers[YEAR][DAY_NUMBER - 1](daysInput[YEAR][DAY_NUMBER - 1], 2);` (`2` for `part2`)

## Test suite

Open `test/index.js` and activate the unit tests you want to run. For example if you want to run all the available tests, make sure the two lines are uncommented and exactly:
```js
runTests(testData2016, 2016);
runTests(testData2018, 2018);
```
Note: Optionally, if you want to skip the unit tests that are considered as too long, you can pass a first argument `true`.

Within the root repository in a terminal, run `npm test`. It will execute two test suites:
- one for `utils` thanks to `mocha`
- one for `days` challenges thanks to a handmade unit test tool

If the test suite is successful you'll see `mocha` results first then the handmade unit test tool's results for each year:
```
24 passing (12ms)

...

Total: 114/114 🎉
Test suite duration: 352767.869ms
```

Note: If you want to run the `mocha` tests exclusively, run `npm run test-utils-only` instead

## Progress

### 2016

|Parts/Days|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25 :christmas_tree:|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|1|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star2:|
|2|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star2:|

### 2018

|Parts/Days|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25 :christmas_tree:|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|1|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|
|2|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|:star:|

## License

:copyright: This repository does not contain any license for now (i.e. there is no `LICENSE.md`). It means that, **for now**, this project does **not** accept contributions.
For more information about it, please read the following [documentation](https://help.github.com/articles/licensing-a-repository/#choosing-the-right-license) stating:
> You're under no obligation to choose a license. However, without a license, the default copyright laws apply, meaning that you retain all rights to your source code and no one may reproduce, distribute, or create derivative works from your work.

The same link also mentions:
> If you're creating an open source project, we strongly encourage you to include an open source license.

Having a license in order to encourage contributions is definitely part of my future plans for this repository. I will probably choose [MIT License](https://choosealicense.com/licenses/mit/) when doing so (this is subject to change). This repository will have a license as soon as Advent of Code 2018 is done (25th of December 2018).

:question: Why not having a license directly at the beginning of the project?

- I plan to use the code I'm producing right now (from this 2016 edition) for the 2018 edition in December 2018 so I can win when competing against my friends. Having no license legally prevents them from being able to use my code :laughing: :ok_hand:

## Memorable challenges

### 2016

#### Easy challenges

- Day 11 part 1 and 2 were pretty easy. I solved them without coding, by simply using a spreadsheet to move cells around.
- Day 22 part 2 was pretty easy and solved in a similar way.

#### Difficult challenges

- Day 9 part 2 was a really tough one
- Day 19 part 2 was a really tough one, as well. This is the only challenge that made me have a look at [reddit](https://www.reddit.com/r/adventofcode/) for a clue as I was stuck for too long.
  - I was trying to find a pattern but it wasn't that obvious. After several attempts then looking at [reddit](https://www.reddit.com/r/adventofcode/), I noticed that people were getting a predictable pattern so I came back to my code and fixed my mistake in order to see it too. Once this thing done, implementing part 2 was not that hard anymore.

### 2018

Coming soon.

## Other years

You can access 2017 repository [here](https://github.com/sebranly/advent-of-code-2017). The reason why 2017 is apart is because I did it in C as it was my first Advent of Code. While C was an interesting choice, it is not the best choice especially for implementation speed (it's a good choice for execution speed though).

|Advent of Code Year|Year I completed it|Completed on time|Language(s) used|Additional notes|
|-|-|-|-|-|
|2015|N/A|:x:|N/A|Not done yet|
|2016|2018|:x:|JavaScript|
|2017|2017|:white_check_mark:|C|
|2018|N/A|N/A|JavaScript|Not done yet|

## Creator

Make sure to follow [Eric Wastl](https://twitter.com/ericwastl) on Twitter, creator of the [Advent of Code](https://adventofcode.com/)