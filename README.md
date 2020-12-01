## CIS4400_project ETL

The Extract, Transform, Load (ETL) documentation will show you the code in different steps of the ETL process by providing a basic explanation and examples of how to do it.

### Installation:
1. Install Python IDE Anaconda Navigator - Jupyter Notebook. The Anaconda documentation below provides instructions to install it based on your operating systems.
- https://docs.anaconda.com/anaconda/install/
2. Install MySQL. The MySQL installation Guide below provides instructions to install it based on your operating systems.
- https://dev.mysql.com/doc/mysql-installation-excerpt/5.7/en/
3. Install Python libraries Pymysql, Pandas and NumPy on Jupyter Notebook using the below commands.
- pip install pymysql
- pip install pandas
- pip install numpy

### Running code in Jupyter Notebook:
1. Jupyter Notebook documentation on how to run code. 
- https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Running%20Code.html

### ETL steps:
1. Extract flat files from Kaggle.com <br>
Download the below files to your computer.
- Netflix IMDB scores https://www.kaggle.com/sarahjeeeze/imdbfile
- Netflix original list https://www.kaggle.com/abhimanyudasarwar/netflix-originals
- Netflix stock data https://www.kaggle.com/aayushmishra1512/netflix-stock-data

2. Transform data <br>
Open Jupyter Notebook in Anaconda and create a Python3 file in the same directory that you saved the flat files to before transforming data.
- Code example for transforming the Netflix original file 
https://github.com/wt051453/CIS4400_project/blob/main/transformation%20of%20netflix_originals.PNG

3. Load data <br>
Create the tables in mysql and load the transformed data into the tables using Python.
- Code example for creating the original_dim table in database and loading data to it 
https://github.com/wt051453/CIS4400_project/blob/main/create_load_original_dim.PNG

### Contribute:
1. Source Code: https://github.com/wt051453/CIS4400_project/blob/main/CIS4400_Group8_ETL.ipynb

### Support:
If you are having issues, please let us know by sending emails to us at wei.tan1@baruchmail.cuny.edu



