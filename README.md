# Sai Rohith Gorla[![](https://img.shields.io/badge/Github-SaiGorla)](https://github.com/SaiGorla)

## Sub Topic: BatchElements
- I have worked on GroupIntoBatches for dataset [games.csv](https://github.com/Rajeshwari-Rudra/apache_beam-python/commit/b0f87e77c581a921b6276649ce68b3ceec0eeb26)
- [My Google Colab Notebook on GroupIntoBatches](https://github.com/Rajeshwari-Rudra/apache_beam-python/blob/main/BatchElements.ipynb)
- [Demonstration Video link](https://app.vidgrid.com/view/IkYnKJI6qefg)
- [My personal repo link](https://github.com/SaiGorla/BatchElements)

## Prerequisites
- Python
- Apache beam
- Google Colab 

## Commands Used 
- First, install apache-beam using the below command.
```
!pip install --quiet -U apache-beam
```
![](https://github.com/Rajeshwari-Rudra/apache_beam-python/blob/main/rohith-images/dependencies.PNG)

- Install the other dependencies 
```
!pip install apache-beam[gcp,aws,test,docs]
```
![](https://github.com/Rajeshwari-Rudra/apache_beam-python/blob/main/rohith-images/dependencies.PNG)

- Program that performs the BatchElement operation
![](https://github.com/SaiGorla/BatchElements/blob/main/images_Sairohith/code.PNG)

- output of the program
![](https://github.com/Rajeshwari-Rudra/apache_beam-python/blob/main/images_Sairohith/output.PNG)

- The command that lists all the files
```
! ls
```
![](https://github.com/Rajeshwari-Rudra/apache_beam-python/blob/main/images_Sairohith/ls.PNG)

- First upload your .csv file to your google drive account.
- The email used should be same for both google drive and google Colab accounts.
- Import the .csv file run into google colab.
![](https://github.com/Rajeshwari-Rudra/apache_beam-python/blob/main/rohith-images/code.PNG)
```
# Code to read csv file into colaboratory:
!pip install -U -q PyDrive
from pydrive.auth import GoogleAuth
from pydrive.drive import GoogleDrive
from google.colab import auth
from oauth2client.client import GoogleCredentials
```
```
# Autheticate E-Mail ID
auth.authenticate_user()
gauth = GoogleAuth()
gauth.credentials = GoogleCredentials.get_application_default()
drive = GoogleDrive(gauth)
```

- To get the id of the file, right-click on the file in google drive account, select share link option, then copy the link.
- Remove the part that contains https://
- keep only the id part.

```
# Get File from Drive using file-ID
# Get the file
downloaded = drive.CreateFile({'id':'1b73yN7MjGytqSP5wimYAQmtByOvGGe8Y'}) # replace the id with id of file you want to access
downloaded.GetContentFile('superbowl-ads.csv') 
```

- Command to add the result to a output file
```
!cat output.txt-00000-of-00001 # output file
```
![](https://github.com/Rajeshwari-Rudra/apache_beam-python/blob/main/images_Sairohith/output.PNG)

## References 
- [Kaggle](https://www.kaggle.com/)
- [Apache-beam](https://colab.research.google.com/github/apache/beam/blob/master/examples/notebooks/get-started/try-apache-beam-py.ipynb)
- [link](https://colab.research.google.com/notebooks)


