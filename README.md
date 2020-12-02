[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)

# GoogleColabLearning
How to use a colab, upload or import data, csv use and import image file will be shown in here.

<h3>Requirements:</h3>

- A google account

- A Kaggle account (necessary)


Description:

Check this link to understand what is colab and how to use it.
<a href="https://towardsdatascience.com/getting-started-with-google-colab-f2fff97f594c"> Google Colab </a>

<h3>Methods</h3>

1st of all install the dependencies.

Then upload the credieentials of the kaggle account. For this, 

   - you have to go to your kaggle account 
   
   - select my account option 
   
   - Scroll down, there will be a row called API , there you will find a option named "create new api"
   
   - save the file.
    
    from google.colab import files
    
    files.upload()
    
   - then upload the saved file from your directory.
   
Before import a dataset, use these code

    !mkdir -p ~/.kaggle

    !cp kaggle.json ~/.kaggle/

    !chmod 600 ~/.kaggle/kaggle.json
    
 More details in this<a href="https://xspdf.com/resolution/50168587.html"> Blog </a> and 
                <a href="https://www.kaggle.com/docs/api"> Kaggle </a>
 
For importing the dataset that you want to use for your project, 
  
   - go to the dataset 
   
   - on the right side, beside the "New Notebook" there will be option,
   
   - click that, you will find a option named "copy api command"
   
   - copy that, and paste it in your code.
   
    !kaggle datasets download -d chiragsoni/ferdata
    (Like This)

If you see a CSV file than use pandas command like 
    
      import pandas as pd 
     
      df = pd.read_csv('filename')
      
      df.head()
      
   Details in <a href="https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html">Here</a>

If you have a zip file, then unzip it first

    !unzip filename
    
For image file, 

    from IPython.display import Image
    
    Image('file')
    
   Details in <a href="https://ipython.org/ipython-doc/dev/api/generated/IPython.display.html"> here (Documentation)</a>,
   <a href="http://www.cs.put.poznan.pl/wjaskowski/pub/teaching/kck/lectures/notebooks/ipython-notebook.html">here (IPython for notebook) </a> and
   <a href="https://towardsdatascience.com/adding-image-files-inside-an-ipython-notebook-python-and-r-2ba089a658b8"> here </a>.
