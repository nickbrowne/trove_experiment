# Trove API Experiment
Updates April 26th 2017

Searches Trove (National Library of Australia) for historical articles matching input town name and search term
Writes results to csv file and then proceeds to read them aloud with the "say_something" method

## Usage
### without instructions read aloud:
```
ruby call_the_olden_days.rb
```
### with instructions read aloud:
```
SAY_EVERYTHING=true ruby call_the_olden_days.rb
```

## Changes
This version only reads instructions if the program is called with the system setting SAY_EVERYTHING=true
It will still read the articles but not the instructions, unless you set this at the start
The idea is that saying the instructions is only entertaining sometimes
This version takes the two search terms DIRECT FROM USER
It does not (as in previous versions) require a csv of town names...
The csv concept is likely to be useful in future, but for live-performance purposes it is too time consuming
The "say_something" method will now work for Mac or for Linus
This version has more direct user input for more flexibility
In particular, it lets the user CURATE articles first, before proceeding to the reading
(this approach won't necessarily work better in the long term, but for live use, flexibility and speed is important)

## Limitations
Does not deal with the full result list from Trove, only the first 100 results per search
This version has more methods rather than line-by-line code, but it is still pretty messy

## TODO:
Search could be more effective for comprehensiveness
e.g. sorting results differently (to avoid repetition), or possibly fetching the whole article rather than the snippet
Clean up more code, it is still a bit messy and some features should be in methods
