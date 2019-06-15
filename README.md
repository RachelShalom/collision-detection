# Collision Detection
### This is a school project done with a company to classify dangerous vs. non dangerous driving on the road. I strted with some exploaration and preprocessing and moved to base models ( Random forest and gradient boosting ) and then tried resnet based on this paper+repo:
https://github.com/hfawaz/dl-4-tsc
### Data:
THe data used for this project belong to the company I did the project for, hence could not upload it here. It contains the following:
- Accelerometer(Csv file @ 50Hz)
- Gyroscope (Csv file @ 50Hz)
- Magnetometer(Csv file @ 50Hz)
- GPS (Csv file @ 1Hz)
### Code
THe following files contained modeling and exploratory analysis:
- [Analyzing GPS Data.ipynb](https://github.com/RachelShalom/collision-detection/blob/master/Analyzing%20GPS%20Data.ipynb): an interactive map of GPS data to see any patterns based on location
- [modeling accel with random forest_-animation of video with bus-.ipynb](https://github.com/RachelShalom/collision-detection/blob/master/modeling%20accel%20with%20random%20forest_-animation%20of%20video%20with%20bus-.ipynb): modeling with randomforest using only accelerometer
- [modeling accel with gradientboosting_-animation of video with bus.ipynb](https://github.com/RachelShalom/collision-detection/blob/master/modeling%20accel%20with%20gradientboosting_-animation%20of%20video%20with%20bus.ipynb): modeling with gradientboosting using only accelerometer 
I created frames for a [gif](https://imgflip.com/gif/33dp6h) showing the gradientboosting predictions https://imgflip.com/gif/33dp6h
- [modeling accel and gyro with gradientboosting.ipynb](https://github.com/RachelShalom/collision-detection/blob/master/modeling%20accel%20and%20gyro%20with%20gradientboosting.ipynb): modeling with 2 sensors
- [modeling GPS accel and gyro with random forest.ipynb](https://github.com/RachelShalom/collision-detection/blob/master/modeling%20GPS%20accel%20and%20gyro%20with%20random%20forest.ipynb): modeling with 3 sensors
### Prerequisites
For the base models all python packages needed are listed in [requirements.txt](https://github.com/RachelShalom/collision-detection/blob/master/requirements.txt) file and can be installed simply using the pip command.
this project was running on Google Deep Learning VM Based on: Debian GNU/Linux 9.8 (stretch) (GNU/Linux 4.9.0-8-amd64 x86_64\n)
- numpy
- pandas
- sklearn
- scipy
- matplotlib
### Results for base models:
|               | Gradientboosting | Random Forest |
| ------------- | ------------- | ------------------|
|Accelerometer  | acc: 79.69% recall: 84% precision:80% | acc: 82% recall: 89% precision:81% |
| Accel+Gyro  | acc: 79.32% recall: 85% precision:78% | acc: 81% recall: 87% precision:79% |            
|Accel+ Gyro +GPS|acc: 82% recall: 88%  precision:81% | acc: 81.57% recall: 88% precision:79% |
 
                         
