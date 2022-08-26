# Reddit_OSINT
Boring Description: A CLI tool for Reddit

Fun Description: Ever wanted to search reddit without being sucked into the hivemind? Well here is your solution! <br>
This simple, easy to use Command Line tool allows you to cut out the BS, and find exactly what you are searchng for on the worlds most toxic
website! (besides twitter) Better yet, if you are a security professional, or a simple script kiddie, you now have access to an OSINT tool that will 
help you get the info you need, and fast!

![image](https://user-images.githubusercontent.com/91687869/184547440-d7ea63fe-d642-4960-b45d-107debeb1fb4.png)

***SETUP***:
 You will need a reddit secret token, client ID and reddit login to use this tool (enter this info into 'config/credentials.json')<br>
 Follow this guide [here](https://12ft.io/proxy?q=https%3A%2F%2Ftowardsdatascience.com%2Fhow-to-use-the-reddit-api-in-python-5e05ddfd1e5c)

***SYNTAX***:  <br>
  **-h**: Help  <br>
  **-s**: Search (use "*" for wildcard/all, and "" for mutli word searches: "RTX 3090 release date"  <br> 
> NOTE: Reddit will search for the exact string first (ex "RTX 3090 release date") and then search based on each word if there are no matches/it runs out of matches to display (ex: RTX, 3090, release, date) <br>

  **-sbr**: Subreddit to search   <br>
  **-vd**: Download videos attached to posts if available (auto sorted by subreddit) <br>
    ![image](https://user-images.githubusercontent.com/91687869/184547697-60864ee2-691d-4def-8316-b5546cb6aa87.png)
    ![image](https://user-images.githubusercontent.com/91687869/184547731-99adb8d8-0119-4732-a4ba-f25375814cdb.png)

  
  
  ***FILTERS***:  <br>
  **--sort**: sort by top, hot, new, controversial, comments <-(most comments)  <br>
  **--time**: Time to filter by: all, year, month, day, hour !! needs -sort flag to work !! <br>
  **--limit**: How many posts to display on screen, max is 100 (NOTE: The higher the limit, the longer the search takes)  <br>
  Alternative Searches:  <br>
  **-u**: Search for a user <br>
  **-c**: Search for a comment (BETA - limited to top level comments only)  <br>
 <br>

***EXAMPLES***:  <br>
**General Usage:** <br>
> python3 reddit_osint.py -s "*" --limit 5 -vd   <br>
 ![image](https://user-images.githubusercontent.com/91687869/185832243-5468563c-1f4b-41c9-88ab-5538ecb09af7.png)
 
**Advanced Usage:** <br>
> python3 reddit_osint.py -s ferrari --sort hot -sbr idiotsincars --limit 30 --time all -vd   <br>
 ![image](https://user-images.githubusercontent.com/91687869/185832130-422d4da7-0aa7-4301-9864-85e07f0d4974.png)

**Email Hunting:** <br>
> python3 reddit_osint.py -s "*@gmail.com" -c <br>
 ![image](https://user-images.githubusercontent.com/91687869/185832385-59d820c9-6cb1-423e-a971-9d099e368b5d.png)


**General Flow Diagram of how it works:** <br>
 ![image](https://user-images.githubusercontent.com/91687869/186959433-a5dfd2a1-0eaa-4a9f-804f-a8e34ef234c5.png)




NOTE: There may be an error with Pandas, Pandas 1.4.3 is the version you need incase you run into any trouble
