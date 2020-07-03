<script type="text/javascript"
src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.2/MathJax.js? 
config=TeX-MML-AM_CHTML"
</script>

<p align="center">
  <h1 align="center">Face Classification and Verification</h1>
</p>

## Introduction
The main goal of this assignment is to familiarize with the proble of Classification of "faces" by using various famous feature extraction and classification methods.

## File Structure
The file structure of the repository is as follows:
```bash
.
├── 20171114.ipynb
├── 20171114_Report.pdf
├── README.md
├── SMAI_M_2019_A2_Final.pdf
├── assets
└── dataset

2 directories, 4 files
```
## :file_folder: Files
### 20171114.ipynb
- This is the ipython notebook containing all the necessary code in **python-3.5**.

### 20171114_Report.pdf
- A report of the various observations and experiments related to the assignment.

### dataset
- This folder contains 3 different kinds of datasets. Each dataset has faces images of humans. The datasets are:
	- **Yale Face Dataset**:
		- Contains face images of 15 subjects.
		- Each subject has 11 images with different emotions.
		- An **emotion.txt** is also present, which contains the mapping of emotions for each image.
	- **Indian Movie Face Database**:
		- Contains face images of 8 Indian movie actors.
		- There are 50 images for each actor.
	- **IIIT Cartoon Face Dataset**:
		- Contains cartoon faces of 8 subjects.
		- 100 images of each subject.

## :runner: Usage
- You can view the python-notebook using [nbviewer](https://nbviewer.jupyter.org/) or [Google Colab](https://colab.research.google.com/).
- Use jupyter to run the python-notebook locally.
```bash
pip install jupyter
jupyter 20171114.ipynb
```

## Summary of Results
There are 5 compoments of the assignments, results of which are summarised below:
### Understanding **Eigen Faces**
- What are eigen faces?
Eigen Faces are the set of eigen-vectors of the covariance-matrix of face images that are used in the problem of human face recognition.

### How many eigen vectors/faces are required to reconstruct a person in the three datasets?
![Eigen-Value Spectrum for the datasets](./assets/eig_compare.png)

- We use the following equation to calculate the number of eigen-vectors ($$k$$) with reasonable accuracy $$\epsilon$$.


$$x_{1,2} = \frac{-b \pm \sqrt{b^2-4ac}}{2b}.$$
<p align="center">
	<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1">
</p>

where $\epsilon = 0.9$ and $[k]$ is the set of selected eigen-vectors and $[j]$ is the set of all eigen-vectors.
