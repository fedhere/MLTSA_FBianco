
# Reading
Sorry ARIMA, but I’m Going Bayesian

https://multithreaded.stitchfix.com/blog/2016/04/21/forget-arima/

# Homework 3

Working with the stock market data we used in class (if anyone of you gets rich, I expect a cut!) use ARIMA models to forecast stock price.
Follow the notebook instructions [ARIMA_instructions.ipynb](https://github.com/fedhere/MLTSA_FBianco/blob/main/HW3/ARIMA_instructions.ipynb)
NOTE: to get the data you need a Kaggle account! look below to see how to integrate your kaggle credentials into a colab notebook


Perform an autoregressive model analysis of Uber rides data with Facebook Prophet, notebook [berprophet_instructions](https://github.com/fedhere/MLTSA_FBianco/blob/main/HW3/berprophet_instructions.ipynb}
NOTE: there is a lot of optional stuff there! Prophet allows you to include exogenous variables in addition to autoregressive elements! 


Please register for an account at kaggle.com, all the work we will do together in class as well as your next homework will require it. To register do the following:

## Kaggle and google drive access instructions
go to kaggle.com

click on “Register” in the upper right corner select either Register with Google, or Register with your email (it’s up to you)
follow the instructions provided by kaggle to create an account (enter your email address, create a password, and choose a username), all of which are up to you, this will be your account after all
Make sure that at the end, you have an account that you can log in with, and be logged in and ready next class


- Go to https://www.kaggle.com/ and sign in

- Click on the icon of your avatar on the top right
  <img width="929" alt="Screen Shot 2023-10-21 at 1 23 01 PM" src="https://github.com/fedhere/FDSFE_FBianco/assets/1696902/2d1a6c89-2230-4398-a9fe-c16fa4dd053e">

- select "Settings" from the drop menu
  <img width="627" alt="Screen Shot 2023-10-21 at 1 28 43 PM" src="https://github.com/fedhere/FDSFE_FBianco/assets/1696902/2d92102f-79ab-4eb7-ae86-f71ca14d706a">

- scroll down to API and click create New API Token. This will download a json file on your computer
  
<img width="654" alt="Screen Shot 2023-10-21 at 1 24 10 PM" src="https://github.com/fedhere/FDSFE_FBianco/assets/1696902/8ab3ae90-9c4d-4ee9-8442-b28dce975fd4">
<img width="855" alt="Screen Shot 2023-10-21 at 1 23 57 PM" src="https://github.com/fedhere/FDSFE_FBianco/assets/1696902/0de116d5-56c2-4024-877d-518972de8a16">

- open google drive at https://drive.google.com/drive/u/0/my-drive in your browser
- upload (e.g. drag and drop) the kaggle.json file from your laptop to the drive **into a folder called .kaggle** (notice that it starts with a "." - that makes it a hidden file which you would not see if you for example ran a bash `ls' command to list files in a folder. Its a very minimal level of cybersecurity)

  <img width="1469" alt="Screen Shot 2023-10-21 at 1 26 51 PM" src="https://github.com/fedhere/FDSFE_FBianco/assets/1696902/c7e27015-34ad-41a8-9f0f-5a816ff5c504">

- the rest of the information are to be done on your colab notebook: follow accordingly

```
# this mounts your google drive
from google.colab import drive
drive.mount("/content/gdrive")

# this gets you to your drive folder
cd gdrive/My\ Drive/.kaggle

# this makes sure the file is there: this cell should return "kaggle.json"
ls kaggle.json

# this limits who can view and make changes who can access this file.
!chmod 600 kaggle.json

# this reads in the file and stores it into the system variables of your colab sessions which allows you to connect programmatically to the kaggle platform

envs = json.load(open("kaggle.json", "r"))
os.environ["KAGGLE_USERNAME"] = envs['username']
os.environ["KAGGLE_KEY"] = envs['key']
```



