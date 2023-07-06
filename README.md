# Analysis-of-climate-change-based-on-machine-learning-and-endoreversible-model
To analyze the complexity of climate change, the planet's land and ocean temperatures are measured. 
This repository will make an analysis of the future terrestrial temperatures analyzed by a thermodynamic modeling of finite times. 
To analyze global warming, the theoretically obtained data was compared with experimental data. 

#######################################################
######################################################
Numerical Solution of Heat Engine (Wolfram Language )
######################################################
########################################################

The following program in Wolfram Language presents the numerical solution
of a Gordon and Zarmi type thermodynamic model that represents a 
Sun-Earth-Wind system as a heat Engine.

#############
##Variables##
#############

t0 = 4.6 10^(9); #Time
\[Sigma] = 5.67 10^(-8); #Stefan–Boltzmann constant
R = 1; #Nonendoreversibility parameter
\[Gamma] = 0.537099021; #greenhouse parameter
\[Rho] = 0.461772791; #albedo parameter

S = (1 + 0.4 (1 - (2079 + t0)/t0))^-1 I0; # luminosity of the Sun
q = (S*(1 - \[Rho]))/4; # average solar radiation flux q per area

#############
##Equations##
#############
We have two equations whose numerical solution provides the highest and lowest layer surface temperatures. 
The low of the Earth's atmosphere under a regime of maximum power in terms of the non-endo reversibility parameter R,
the albedo $\rho$, the greenhouse effect $\gamma$, and the current solar constant $I_sc$.


ap = T_1^{5}-T_{2}T_1^{4}-\frac{2\bar{q_s}}{3R\sigma(1-\gamma)}T_2=0

bp = T_{1}^4+\frac{1}{(1-\gamma)}T_{2}^3T_{1}
-\frac{\bar 2q_s}{R\sigma (1-\gamma)}

#############
##Solution##
#############

sol = Solve[{ap == 0, bp == 0}, {T_1, T_2}];

Only the real and positive solutions should be taken, then it is necessary to consider the dissipation with the following equations

T1 = 306.296
T2 = 199.782
n = 1 - Sqrt[(T2/T1)]^(0.5)
Q1 = (T1 - T2 - T1*n)/1 - n
a = T1*(1 - n) - T2
b = (1 - n)*T1 + T2
Q2 = T2*(a/b)
phi = Q2 - (T2/T1)*Q1
TF = T1 + phi

It is important to note that to make these calculations all the variables are in degrees Kelvin, with this we can calculate
the temperatures per year and compare it with the results of the dataset.

#######################################################
######################################################
Datasets
######################################################
########################################################

The data compilation by Berkeley records Land Average temperatures in the format yyyy/mm/dd. So, a split was made by year, 
month, and day taking the temperature of each month, and the mean temperature per year was computed. It is observed that 
there is a correlation with a value of 0.89 between the variables of the year and the Land Average Temperature from the year 1975 to 2015 

1.- GlobalTemperaturesGZ.csv.

 Table presents the future prediction of the temperatures using linear regression (LR), Ridge Regression (RR), and Artificial Neural Networks (ANN). 
 All techniques were applied to the observed temperatures (Tobs) and the models’ temperatures used in the present work. In the same way, the third column 
 shows the temperatures calculated (Ts) from our model of Gordon and Zarmi (GZM) without applying a linear regression, where the physical characteristics 
 of the atmosphere are taken into account and what theoretical temperature would be reached. In addition, Table depicts the entire prediction made up to 2100, 
 starting in 2016

2.- FinalGraphTemp.csv

#############
##Notebooks##
#############

In the notebooks, an Exploratory Data Analysis of the data set is carried out, to later make a comparison through machine learning techniques.
