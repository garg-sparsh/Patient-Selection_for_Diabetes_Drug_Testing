# Patient-Selection_for_Diabetes_Drug_Testing

Context: Its a project for exciting unicorn healthcare startup that has created a groundbreaking diabetes drug that is ready for Phase III clinical trial testing. It is a very unique and sensitive drug that requires administering and screening the drug over at least 5-7 days of time in the hospital with frequent monitoring/testing and patient medication adherence training with a mobile application. I have been provided a patient dataset from a client partner and are tasked with building a predictive model that can identify which type of patients the company should focus their efforts testing this drug on. Target patients are people that are likely to be in the hospital for this duration of time and will not incur significant additional costs for administering this drug to the patient and monitoring.

In order to achieve the goal a regression model must be created that can predict the estimated hospitalization time for a patient and use this to select/filter patients for the study.

Expected Hospitalization Time Regression Model: Utilizing a synthetic dataset(denormalized at the line level augmentation) built off of the UCI Diabetes readmission dataset, We will build a regression model that predicts the expected days of hospitalization time and then convert this to a binary prediction of whether to include or exclude that patient from the clinical trial.

This project will demonstrate the importance of building the right data representation at the encounter level, with appropriate filtering and preprocessing/feature engineering of key medical code sets. This project will also require students to analyze and interpret their model for biases across key demographic groups.

Dataset
Due to healthcare PHI regulations (HIPAA, HITECH), there are limited number of publicly available datasets and some datasets require training and approval. So, for the purpose of this exercise, we are using a dataset from UC Irvine that has been modified for this project. Please note that it is limited in its representation of some key features such as diagnosis codes which are usually an unordered list in 835s/837s (the HL7 standard interchange formats used for claims and remits).

https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008
Getting Started
Follow the instructions in starter_code/main_project.ipynb and be sure to set up your Anaconda environment to get started!

Dependencies
Using Anaconda consists of the following:

Install miniconda on your computer, by selecting the latest Python version for your operating system. If you already have conda or miniconda installed, you should be able to skip this step and move on to step 2.
Create and activate * a new conda environment.
* Each time you wish to work on any exercises, activate your conda environment!

1. Installation
Download the latest version of miniconda that matches your system.

Linux	Mac	Windows
64-bit	64-bit (bash installer)	64-bit (bash installer)	64-bit (exe installer)
32-bit	32-bit (bash installer)		32-bit (exe installer)
Install miniconda on your machine. Detailed instructions:

Linux: http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
Mac: http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
Windows: http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install
2. Create and Activate the Environment
For Windows users, these following commands need to be executed from the Anaconda prompt as opposed to a Windows terminal window. For Mac, a normal terminal window will work.

Git and version control
These instructions also assume you have git installed for working with Github from a terminal window, but if you do not, you can download that first with the command:

conda install git
If you'd like to learn more about version control and using git from the command line, take a look at our free course: Version Control with Git.

Now, we're ready to create our local environment!

Clone the repository, and navigate to the downloaded folder. This may take a minute or two to clone due to the included image data.
git clone https://github.com/garg-sparsh/Patient-Selection_for_Diabetes_Drug_Testing.git
cd nd320-c1-emr-data-starter/project/
Create (and activate) a new environment, named diabetes_drug_testing. If prompted to proceed with the install (Proceed [y]/n) type y.

Linux or Mac:
conda create -n diabetes_drug_testing python=3.7
source activate diabetes_drug_testing
Windows:
conda create --name diabetes_drug_testing python=3.7
activate diabetes_drug_testing
At this point your command line should look something like: (diabetes_drug_testing) <User>:USER_DIR <user>$. The (diabetes_drug_testing) indicates that your environment has been activated, and you can proceed with further package installations.

Install a few required pip packages, which are specified in the requirements text file. Be sure to run the command from the project root directory since the requirements.txt file is there. I also added a line for installing the environment in your notebook in case this is new for you. You should be able to now look for the environment when you select the kernel.

pip install -r requirements.txt
ipython3 kernel install --name diabetes_drug_testing --user

License
This project is licensed under the MIT License - see the LICENSE.md
