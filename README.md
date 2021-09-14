## ** predicting heart disease using machine learning **
### this notebook looks into using various python-based machine learning and data science libraries in an attempt to build a ML model capable of predicting whethernor not someone has heart disease based on their medical attributes.

1. problem definition
2. data
3. evaluation
4. features
5. modelling
6. experimentation


 
## 1. problem definition
In a statement, 
> given clinical parameters about a patient, can we predict whether or not they have heart disease?


## 2. data
the original data come from Cleavland, UCL ML Repository. 


## 3. evaluation
> if we can reach 96% accuracy at predicting whethe or not a patient has heart disease during the proof of concept, we'll pursue the project


## 4. features
Features are different parts of the data. During this step, you'll want to start finding out what you can about the data.

>One of the most common ways to do this, is to create a data dictionary.

>Heart Disease Data Dictionary
A data dictionary describes the data you're dealing with. Not all datasets come with them so this is where you may have to do your research or ask a subject matter expert (someone who knows about the data) for more.

>The following are the features we'll use to predict our target variable (heart disease or no heart disease).

age - age in years
sex - (1 = male; 0 = female)
cp - chest pain type
0: Typical angina: chest pain related decrease blood supply to the heart
1. Atypical angina: chest pain not related to heart
2. Non-anginal pain: typically esophageal spasms (non heart related)
3. Asymptomatic: chest pain not showing signs of disease
trestbps - resting blood pressure (in mm Hg on admission to the hospital)
anything above 130-140 is typically cause for concern
chol - serum cholestoral in mg/dl
serum = LDL + HDL + .2 * triglycerides
above 200 is cause for concern
fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
'>126' mg/dL signals diabetes
restecg - resting electrocardiographic results
0. Nothing to note
1. ST-T Wave abnormality
can range from mild symptoms to severe problems
signals non-normal heart beat
2. Possible or definite left ventricular hypertrophy
Enlarged heart's main pumping chamber
thalach - maximum heart rate achieved
exang - exercise induced angina (1 = yes; 0 = no)
oldpeak - ST depression induced by exercise relative to rest
looks at stress of heart during excercise
unhealthy heart will stress more
slope - the slope of the peak exercise ST segment
0. Upsloping: better heart rate with excercise (uncommon)
1. Flatsloping: minimal change (typical healthy heart)
2. Downslopins: signs of unhealthy heart
ca - number of major vessels (0-3) colored by flourosopy
colored vessel means the doctor can see the blood passing through
the more blood movement the better (no clots)
thal - thalium stress result
3. normal
6. fixed defect: used to be defect but ok now
7. reversable defect: no proper blood movement when excercising
target - have disease or not (1=yes, 0=no) (= the predicted attribute)
Note: No personal identifiable information (PPI) can be found in the dataset.

It's a good idea to save these to a Python dictionary or in an external file, so we can look at them later without coming back here.

Preparing the tools:
>At the start of any project, it's custom to see the required libraries imported in a big chunk like you can see below.

>However, in practice, your projects may import libraries as you go. After you've spent a couple of hours working on your problem, you'll probably want to do some tidying up. This is where you may want to consolidate every library you've used at the top of your notebook (like the cell below).

>The libraries you use will differ from project to project. But there are a few which will you'll likely take advantage of during almost every structured data project.

1. Pandas for data analysis
2. NumPy for numerical operations.
3. Matplotlib/seaborn for plotting or data visualization.
4. Scikit-Learn for machine learning modelling and evaluation.
