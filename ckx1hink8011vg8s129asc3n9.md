## How I add Hashnode to the list of technology in Wappalyzer

what is a Wappalyzer?,

Wappalyzer is a tool in the form of a website or browser extension to detect the technology that runs behind a website, by using this tool we can find out and peek at various technologies on a website.

Wappalyzer also opens the source code on GitHub so we can contribute to the project, the last few days I checked my Hashnode blog and it turns out that no one has submitted and hasnode has not been detected by Wappalyzer, that's why I contributed to Wappalyzer and submitted some regular expression code to detect Hashnode blog technology. 

to contribute in Wappalyzer is also fairly simple and easy, here are the steps:
1. open the [Wappalyzer repository](https://github.com/AliasIO/wappalyzer)  on GitHub.
2. read the documentation and pattern files of the project in the README file so we can better understand how Wappalyzer works.
3. read the CONTRIBUTING.md file so we can know how to contribute to the project properly.
4. fork the Wappalyzer repository.
5. because Hashnode starts with the letter H that's why I put the RegEx script in the [h.json](https://github.com/AliasIO/wappalyzer/blob/master/src/technologies/h.json)  file.
6. this is the script I added :
```json
"Hashnode": {
    "cats": [
      11
    ],
    "description": "Hashnode is a free developer blogging platform that allows you to publish articles on your own domain and helps you stay connected with a global developer community.",
    "dom": "div.css-zigog8",
    "icon": "hashnode.png",
    "scriptSrc": "hashnode\\.com",
    "url": "^https?://[^/]+\\.(?:hashnode)\\.dev",
    "website": "https://hashnode.com/"
  },
``` 
7. add icon file from Hashnode in [icon folder](https://github.com/AliasIO/wappalyzer/tree/master/src/drivers/webextension/images/icons)
8. commit all the changes you made in the project you forked after all, do a pull request to the Wappalyzer repository.
9. Wait until you get your request merged by the repository owner, it won't take long.

and yes the process is complete and you have contributed to a large open source project, be of use.

Thank you for reading my article, if you have any suggestions or questions, I am very open to that, please use the comments column.
