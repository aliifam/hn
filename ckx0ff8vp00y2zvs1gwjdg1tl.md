## How to Manipulate GitHub Activity?


> disclaimer: I made this project with the aim of having fun and to learn to automate things using the Python language

Have you ever seen the activity timeline on someone's GitHub profile is very green and looks very active and consistent?

Do you want to make your GitHub profile very consistent even though it has been less green in the past?

From this :
![unactive-commit.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1639130723281/y4FMp_0BW7.png)


To this :

![active-commit.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1639130675466/iQUQN_wHZ.png)

take it easy, I have a solution, you can use a program that I made using Python 3 language, by using this script you can modify the timeline of your activities in the past until now to be very green and consistent.

repository link : [GitHub Activity Generator](https://github.com/aliifam/github-activity-generator) 

## How to use?
1. Make sure in your Machine already installed Python 3.6 + and Git.
2. Make sure Git in in your Machine already configured with Github.
3. create an empty Github Repository can public or private, but I prefer you to make it private. **do not initialize it**.
4. Download the [main.py script](https://github.com/aliifam/github-activity-generator/archive/main.zip) and open the file in your text editor.
5. delete the file **commit.txt**
6. customize the script in main.py for configuration as you want in here:
```python
total_day = 366 #total days back
commit_frequency = 10 #commit time per day
repo_link = "https://github.com/aliifam/github-activity-generator.git"
```
7. after the script is already, you just run the script and see the magic.
8. the script will make a new commit.txt file and make very many commit as you want after the process finished the script will push the repository to GitHub.
9. after all the process is successful, please press the star for this repository😊.

## How the Program Works?

This simple program basically uses a nested while loop, the first loop to move from day to day and the loop inside to do several commits in one day, then in the commit date manipulation this program uses the python datetime module and to switch days using the timedelta function with the parameter number of days which keeps decreasing with every iteration.

```python
while tl > 0:
    ct = commit_frequency
    while ct > 0:
        f = open("commit.txt", "a+")
        l_date = now + datetime.timedelta(days=-pointer)
        formatdate = l_date.strftime("%Y-%m-%d")
        f.write(f"commit ke {ctr}: {formatdate}\n")
        f.close()
        os.system("git add .")
        os.system(f"git commit --date=\"{formatdate} 12:15:10\" -m \"commit ke {ctr}\"")
        print(f"commit ke {ctr}: {formatdate}")
        ct-=1
        ctr+=1
    pointer+=1
    tl-=1
``` 
very simple right?

you can see the complete script in  [here](https://github.com/aliifam/github-activity-generator/blob/main/main.py) 

## Closing
thank you for reading my sari article, if there are suggestions, criticisms or questions I am very open to it, please use the comments column