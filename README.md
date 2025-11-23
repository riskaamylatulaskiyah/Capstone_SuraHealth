# SuraHealth

# K-means Clustering using Tensorflow
# Team Profile
## Team ID: C23-PC684
 - (ML) M166DSY3397 – Riska Amylatul Askiyah – Universitas Diponegoro - Active
 - (ML) M038DKY4372 – Michelle Cintania Antontte M – Institut Teknologi Sepuluh Nopember - *Inactive*
 - (ML) M340DSY0356 – Bela Ismawati Nuraisa – Universitas Sebelas Maret - Active
 - (CC) C168DSX3435 – Riyan Saputra – Universitas Esa Unggul - Active
 - (CC) C149DSX3695 – Arnaldi Arif – Universitas Bina Nusantara - Active
 - (MD) A163DSX2739 – Pandji Alam – Universitas Dian Nuswantoro - Active

## Project Background:
- Themes:
  Post-Pandemic & Emergency Responses
- Title of the Project:
  SuraHealth
- Abstract:
  This project is important to complete. Project background information highlights the importance of timely access to emergency medical services and the challenges many cities in Indonesia face in ensuring this access. The team wanted to address this issue because they believe that access to emergency medical services is a fundamental right, and it is important to ensure that every citizen can access these services when needed.

This project aims to identify the number of emergency rooms available in Surakarta, their location, and the capacity of these rooms. The team will also analyze emergency room accessibility for different populations and identify access barriers. Finally, the team will provide recommendations to increase the availability and accessibility of emergency medical services in Surakarta.

## Business Understanding
### Problem Statements
  Recently, People had difficulty getting first aid, especially when someone is in another area. We innovated to make an application for one of the cities in Indonesia,  that is Surakarta regarding the availability of ambulances and/or first aid through the chat feature with a general practitioner at the nearest hospital using hospital recommendations location-based. Apart from that, this project was also initiated because of the difficulty for the community in finding information on the capacity of beds or inpatient rooms and hospital emergency rooms. Our team also hopes that this application can make it easier for the people of Surakarta to receive information on the location of the nearest hospital and the first treatment that can be done based on the patient's condition at that time.
This project aims to analyze the availability of emergency rooms in Surakarta using data from SIRANAP, the National Hospital Registry database. The problem statement is that Surakarta, like many other cities in Indonesia, faces challenges in ensuring all residents have access to emergency medical services. The research questions focused on the distribution of emergency rooms in Surakarta, the capacity of the rooms, and how accessible they are to different populations.

###  Goals
  This project has had a good impact on the community, especially around Surakarta.
- The difficulty of finding the nearest hospital according to the type and taste of BPJS can be overcome. This project can provide recommendations for the closest hospital and identify the number of emergency rooms available in Surakarta, their location, and the capacity of the room.
- Difficulty getting hospital contacts can be overcome. Apart from recommending hospitals, we also provide hospital profiles, one of which is a Whatsapp number that can be contacted.
- Limited knowledge of the general public regarding initial steps that can be given to relatives if an incident is resolved. We also designed a <first aid kit> that provides initial maintenance information that can be performed while waiting for the repair team to arrive.

### Content
The repository contains the following files and directories:
- `Dataset\` : A directory containing datasets
- `Model\` : A directory containing the progam code
- ```README.md``` : A markdown file describing the project
- `Data Rumah sakit Fiks di Surakarta.csv` : The dataset containing hospital information including longitude and latitude
- `First Aid.csv` : The dataset contains the name of the disease and the initial treatment method
- `api.py` : Python script to build a simple API as an endpoint for using machine learning models.
- `requirements.txt` : Contains a list of important libraries for the project.

### Data Understanding
We use the Hospital dataset that we collect ourselves. Hospital data comes from the Ministry of Health`s SIRANAP web scraping and manual input.
In total, we use 19 Hospitals with 105 entries and 14 columns, with an initial data type of 2 float columns, 2 integer columns, and 10 object columns.
- `Kode Rumah Sakit`: Hospital Code
- `Type` : classification of General Hospitals based on the Minister of Health of the Republic of Indonesia Number 3 of 2020 Chapter III Pasal 16
- `Kelas` : types of rooms based on the functions and facilities provided
- `Kamar` : the names of the sub rooms that still have free space
- `Jumlah Bed` : the amount of free space available in a Class(“Kelas”)
- `BPJS` : give information 0: can use BPJS and 1: cannot use BPJS
- `No WhatsApp` : emergency/hotline/service contact of the hospital 
- `Foto Rumah Sakit` : hospital photo
- `Longitude` : the longitude of the hospital point
- `Latitude` : the latitude of the hospital point

### Data cleaning
Based on the results, there are missing values in the email and class columns. We also specified the fields we didn`t need and then removed the email and room features.

### Data Preparation
Based on visualizing the data distribution using boxplots, there are no outliers in the latitude and longitude columns.
We also provide weighting for `Longitude` and `Latitude` because we prioritize these factors more than `Type of Bed` and `BPJS.`


## Modelling
### Approach
In this section, I will explain the two main parts of this project, namely providing the first aid feature and the closest hospital recommendation feature based on latitude as the main factor and supported by "hospital type" and "BPJS" factors using the K-meaning Clustering approach with Tensorflow.
approach with scaling and without scaling we do. The scaling feature serves to give weight to the "Longitude" and "Latitude" features because we expect distance to be the main recommendation factor, compared to "Hospital Type" and "BPJS".

We use matriks silhoutte with k optimal = 6
Library yang kita gunakan yaitu Scikit Learn dan Tensorflow.
Kita menggunakan python programming language dengan tools adalah VScode.


