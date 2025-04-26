<h1 align="center">DataFrames & Datasets</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-green" alt="Pandas Badge" />
  <img src="https://img.shields.io/badge/Python-3.9-blue" alt="Python Badge" />
  <img src="https://img.shields.io/badge/Datasets-King%20County%2C%20Population%2C%20Netflix-orange" alt="Dataset Badge" />
</p>

<hr>

<h2>📜 About The Repositry</h2>

<p>
This Repositry focuses on exploring and analyzing multiple datasets using Python's <strong>Pandas</strong> library. 
We explore real estate sales, state population estimates, and Netflix media titles by loading them from CSV files, 
handling different data formats, and preparing them for deeper analysis.
</p>

<hr>

<h2>📂 Datasets Used</h2>

<ul>
  <li><strong>🏡 King County House Sales</strong> - House sale prices and features in King County, WA.</li>
  <li><strong>🌎 State Population Estimates (2020)</strong> - US state population data from 2010 to 2020.</li>
  <li><strong>🎬 Netflix Titles</strong> - Metadata about Netflix shows and movies.</li>
</ul>

<hr>

<h2>🛠 Technologies Used</h2>

<ul>
  <li><strong>Python</strong> - Programming Language</li>
  <li><strong>Pandas</strong> - Data Loading and Manipulation</li>
  <li><strong>Google Colab / Jupyter Notebook</strong> - Development Environment</li>
</ul>

<hr>

<h2>🚀 How To Run</h2>

<ol>
  <li>Mount Google Drive using <code>drive.mount('/content/drive')</code>.</li>
  <li>Set the base dataset path, e.g., <code>/content/drive/MyDrive/Dataset</code>.</li>
</ol>

<h3>📥 Loading Datasets</h3>

<p><strong>1. King County House Sales</strong></p>

<pre>
<code>
from pathlib import Path
import pandas as pd

def load_dataset(filename, base_dir='/content/drive/MyDrive/Dataset', **kwargs):
    return pd.read_csv(Path(base_dir) / filename, **kwargs)

houses = load_dataset('kc_house_data.csv')
houses.head()
</code>
</pre>

<p><strong>2. State Population Estimates</strong></p>

<pre>
<code>
# Providing custom column names
names = [
    'sumlev', 'region', 'division', 'state', 'name', 
    'census2010pop', 'estimatesbase2010', 'popestimate2010', 
    'popestimate2011', 'popestimate2012', 'popestimate2013', 
    'popestimate2014', 'popestimate2015', 'popestimate2016', 
    'popestimate2017', 'popestimate2018', 'popestimate2019', 
    'popestimate042020', 'popestimate2020'
]

state_population = load_dataset("nst-est2020.csv", names=names)
state_population.head()

# Alternatively, loading without custom names
state_population = load_dataset("nst-est2020.csv")
state_population.head()

# Quick info about the dataset
state_population.info()
</code>
</pre>

<p><strong>3. Netflix Titles</strong></p>

<pre>
<code>
# Read the Netflix dataset which uses '|' instead of ',' as separator
# Also set the first column as the index column

netflix = load_dataset("netflix_titles.csv", sep="|", index_col=0)
netflix.head()
</code>
</pre>

<h4>✅ Note:</h4>
<p>
The <code>netflix_titles.csv</code> file is separated by a <strong>pipe (|)</strong> character instead of commas. 
We handle this using <code>sep="|"</code> in the <code>read_csv</code> function.
Additionally, <code>index_col=0</code> sets the first column as the DataFrame index.
</p>

<br><br><br>
<!-- Contact Section --> 

<h3 align="center">Connect with me:</h3>
<p align="center">
       <a href="mailto:safwannasir49@gmail.com" target="blank">
        <img align="center" src="https://www.svgrepo.com/show/484206/mail.svg" alt="safwannasir49@gmail.com" height="30" width="40" />
    </a>
    <a href="https://twitter.com/SafwanNasir49" target="blank">
        <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="safwannasir" height="30" width="40" />
    </a>
    <a href="https://linkedin.com/in/safwan-nasir-955745219" target="blank">
        <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="safwa_nasir" height="30" width="40" />
    </a>
    <a href="https://github.com/safwannasir49" target="blank">
        <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/github.svg" alt="safwannasir49" height="30" width="40" />
    </a>
</p>

<br/><br/>

<hr>
