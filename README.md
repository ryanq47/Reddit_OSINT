# Reddit_OSINT
A CLI tool for Reddit

![image](https://user-images.githubusercontent.com/91687869/184547440-d7ea63fe-d642-4960-b45d-107debeb1fb4.png)

SETUP:
 You will need a reddit secret token, client ID and reddit login to use this tool (enter this info into 'config/credentials.json')<br>
 Follow this guide [here](https://12ft.io/proxy?q=https%3A%2F%2Ftowardsdatascience.com%2Fhow-to-use-the-reddit-api-in-python-5e05ddfd1e5c)

SYNTAX:  <br>
  **-h**: Help  <br>
  **-s**: Search (use "*" for wildcard/all, and "" for mutli word searches: "RTX 3090 release date")  <br>
  **-sbr**: Subreddit to search   <br>
  **-vd**: Download videos attached to posts if available (auto sorted by subreddit) <br>
    ![image](https://user-images.githubusercontent.com/91687869/184547697-60864ee2-691d-4def-8316-b5546cb6aa87.png)
    ![image](https://user-images.githubusercontent.com/91687869/184547731-99adb8d8-0119-4732-a4ba-f25375814cdb.png)

  
  
  Filters:  <br>
  **--sort**: sort by top, hot, new, comments <-(most comments)  <br>
  **--time**: Time to filter by: all, year, month, day, hour !! needs -sort flag to work !! <br>
  **--limit**: How many posts to display on screen, max is 100 (NOTE: The higher the limit, the longer the search takes)  <br>
  Alternative Searches:  <br>
  **-u**: Search for a user <br>
  **-c**: Search for a comment (BETA - limited to top level comments only)  <br>
 <br>

EXAMPLES:  <br>
python3 reddit_osint.py -s ferrari --sort hot -sbr idiotsincars --limit 30 --time all -vd   <br>
or  <br>
python3 reddit_osint.py -s "*" --limit 5 -vd   <br>
or  <br>
python3 reddit_osint.py -s "*"  <br>

NOTE: There may be an error with Pandas, Pandas 1.4.3 is the version you need incase you run into any trouble
