# Predicting remaining useful life of aircrafts' turbofan engines  
Fernando Martinelli Ramacciotti  
fernandoramacciotti@gmail.com

*Udacity's Machine Learning Nanodegree capstone project

Predicitve maintenance through predicting remaining useful life (RUL) of an asset is desired for every business. Data-driven approaches can yield good results, but such data is costly to collect, once companies would lose money to run their machines to failure. NASA has simulated several run-to-failure conditions for a fleet of turbofan engines and such dataset is widely used as a benchmark for developing predictive asset maintenance algorithms. The dataset has 249 training units and 248 testing units with 21 sensors measurements and 3 operational settings that yields six operational regimes. All training units were simulated run-to-failure, while the testing series are cut off sometime before failure. We have used regression and classification machine learning models for estimating RUL and predicting a failure upon the next 20 cycles, respectively. Preprocessing was key to untrap clear trends over time and remove useless features. Moreover, we postprocess regression output with Kalman filter to remove noisy predictions and incorporate domain knowledge. Our models performed relatively well on training set but up to 3 times worse on test. The main reason for such spread is due to the fact that our models performed well when the engines are close to failure and sensors operates at a fairly constant range within each operational mode while the engine is healthy and only deviates when unhealthy. This adds up a degree of complexity, since for healthy engines most of sensor variation is due to noise.

In order to reproduce the research, the following packages are needed:
- pandas==0.23.4
- matplotlib==2.0.2
- numpy==1.14.5
- seaborn==0.9.0
- scikit_learn==0.20.0

The notebook with exploratory data analysis and model development can be found [here](./code/TurboFanAnalysis_v2.ipynb).

The final paper can be found [here](./paper/Ramacciotti2018_PredictingRUL.pdf).