# Rainbow Six Siege Y2S1 Dataset Analysis
Using data collected by Ubisoft and published in the first and final entry in the Data Peek series for Tom Clancy's Rainbow Six Siege, this project analyses all data regarding a player and the current round to determine something.

This analysis was completed with two models: K-Nearest Neighbour and a Neural Network.
The KNN model determines a user's platform based on the data mentioned before.
The Neural Network model determines a user's rank, once again based on the data mentioned.

Different objectives were chosen to make the most of the large dataset and the variety of subjects that could be predicted with it.

## Dataset
This dataset was published by Ubisoft in a blog post titled "[Introduction to the Data Peek: Velvet Shell Statistics](https://www.ubisoft.com/en-us/game/rainbow-six/siege/news-updates/2fQ8bGRr6SlS7B4u5jpVt1/introduction-to-the-data-peek-velvet-shell-statistics)".

This project utilises the second data file published, "Objectives Data".
This file consists of maps, objective locations, player ranks and operators, and all together how they performed.
It was chosen for its size and contents.

### Data Cleaning
The data has been slightly modified before being read.
The original file contained non-ASCII characters, preventing Pandas from being able to read the CSV.

The character was removed with the following command:
```bash
cat -v datadump_S5_summary_objectives.csv | sed 's/M-\^V //' | sed 's/\^M//' > datadump_S5_summary_objectives-cleaned.csv
```

## Libraries
This project makes use of the following libraries:
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [scikit-learn](https://scikit-learn.org/)
- [TensorFlow](https://www.tensorflow.org/)
- [Matplotlib](https://matplotlib.org/)

## Acknowledgements
This project would not have been done if it weren't for Dr Jake Lee assigning it as a final project for his ITCS 3156 - Introduction to Machine Learning course at UNC Charlotte.
The objective of the project was to go out, find a dataset we were interested in, and learn from it.

Additionally, it would not have been possible without my friend Devdan supporting me along the way.
