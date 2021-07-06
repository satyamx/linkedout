# LinkedinBot - Automating the process of applying and getting referrals easier


### Overview

It consists of three stages

#### Stage 1

- in the first Stage the bot fetches the list of all people working in your dream companies and stores them in a csv file


#### Stage2

- In the second stage the bot goes into all the profiles of the persons from the first stage and scraps all their previous experiences including the company Name, Duration and their work details and store them in a csv file


#### Stage3

- In the third stage we retrieve the data of the companies from the second stage and we basically clean the data from the second stage to remove stop words such as Full-time, part-time, contract etc. after cleaning the data we go into each company people section on linkedin and send a customized connection request to all the people working there with a note and your resume.

### Requirements

- Python3
- Selenium
- Beatiful Soup
-
- Note: Use the chromedriver uploaded in the driver directory of this repo. Not using this version of chromedriver might throw exceptions due to incompatibility between the version of the binaries. 

### Installation

- Clone the respository using the command `git clone https://github.com/satyamx/linkedout.git`  
- Install all the dependencies using `pip3 install -r requirements.txt`

### Run it on Local Machine

- In the config.py file add your Linkedin Username, Linkedin Password ,the customized message you want to send and the your dream companies
- For the stage 1 - run the command `python3 stage1.py`
- For the stage 2 - run the command `python3 stage2.py`
- For the stage 3 - run the command `python3 stage3.py`

- Also, the driver used is set through path (in `login.py`), so make sure you are in the `linkedout` directory and executing `pyhton3 stage1.py` and not `./<some_path>/linkedout/stage1.py` (this will throw errors) .

### Caution

- Linkedin monitors the number of profiles you view and the amount of connection request you send.
- I strongly recommend you not to visit more than 1000 profiles and not send more than 100 connection request per week
- To prevent this i have have added a checker which will break the loop if you exceed the above limits
- In case of not obeying the caution, LinkedIn will send you a warning

### To-Do

- Create a web based interface

### I hope you lend to your dream company soon, keep patience and best of luck for the further process
