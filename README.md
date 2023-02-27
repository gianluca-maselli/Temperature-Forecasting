# Temperature-Forecasting

In this notebook both **single-step** and **multi-step forecasting** are performed to predict temperatures of [major cities in the world](https://www.kaggle.com/datasets/sudalairajkumar/daily-temperature-of-major-cities). Due to the fact that it is possible to use the daily average of temperature, the choices made are:
- for single-step predictions, 7 past observations are taken to predict the next day average temperature. 
- for multi-step predictions, 30 past observation are taken to predict the average temperatures for the next 30 days.

To improve the model predictions, **differencing** and **moving average** are used. After pre-processing of the data, the latter are fed to: 
- **Bidirectional GRU**  with one layer followed by a **single fully-connected** layer for single-step predictions.
- **Bidirectional LSTM**  with one layer followed by **two fully-connected** layers for multi-step predictions.

The plots both for single-step and multi-step forecasting are present, however, must be said, that they refers to the city of Rome, which is the one we have choosen to carry out the project. 
