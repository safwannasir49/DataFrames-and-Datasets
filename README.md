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
<!-- Contact Section --> 

<h2 align="center" style="margin-bottom: 30px;">🤝 Cᴏɴɴᴇᴄᴛ Wɪᴛʜ Mᴇ 🤝</h2>
<div align="center" style="margin-bottom: 30px;">
  <a href="mailto:safwannasir49@gmail.com" target="_blank" style="margin: 0 15px;">
    <img src="Images/gmail.png" width=50 height=50 alt="safwannasir49@gmail.com" />
  </a>

  <a href="https://x.com/safwannasir49" target="_blank" style="margin: 0 15px;">
    <img src="Images/twitter.png" width=50 height=50 alt="safwannasir49" />
  </a>

  <a href="https://www.instagram.com/safwan_nasir_" target="_blank" style="margin: 0 15px;">
    <img src="Images/instagram.png" width=50 height=50 alt="safwannasir49" />
  </a>

  <a href="https://www.github.com/safwannasir49" target="_blank" style="margin: 0 15px;">
    <img src="Images/github.png" width=50 height=50 alt="safwannasir49" />
  </a>

  <a href="https://www.linkedin.com/in/safwannasir49/" target="_blank" style="margin: 0 15px;">
    <img src="Images/linkedin.png" width=50 height=50 alt="linkedin" />
  </a>
</div>

<br/><br/>

<hr>
