![alt tag](https://sigvoiced.files.wordpress.com/2016/07/pewter.png)
# Pewter

**Pewter** is an open-source project for <br/>
        **1. Data acquisition**<br/>
        **2. Analysis**<br/>
        **3. Visualisation <br/>**
of raw data from Myo and conduct experiments on it. If you are working on raw data from the Myo Armband, then you can make use of **Pewter's** simple GUI to acquire data and work on it. It not only reduces devlopement time but also makes the life of a machine learning engineer easier. You can create experiments and visualise the data for doing some analysis before preprocessing and feature extraction. All the experiment data will be saved in Json format which makes it even convenient for reuse. The entire project is created using Node.js and I thank [Thalmiclabs](https://www.thalmic.com/) for the [myo.js](https://github.com/thalmiclabs/myo.js) library which made my life a lot more simpler.

**Pewter** was originally developed by me for data acquisition and analysis of raw data from Myo Armband for one of my projects **[Voice](https://github.com/sigvoiced/Voice)**.

I would be glad if you could contribute in this initiative of mine to help other developers working on Myo Armbands and making their lives easier.

#Prerequisites
1. [Node.js](https://nodejs.org/en/)

#Installation
1. Install dependencies : Enter the following command inside the **pewter** folder that you have cloned
```
npm install
```
![alt tag](https://sigvoiced.files.wordpress.com/2016/07/screenshot-49.png)

2. Run Pewter : Enter the following command in the **pewter** directory to start **pewter** 
```
node app.js
```
![alt tag](https://sigvoiced.files.wordpress.com/2016/07/screenshot-50.png)

**The app by default listens to port 3000. To change it to any other port update the listener in the the app.js file and restart.**

3. Start Using Pewter : Open any browser and open the following link to start **Pewter**.
```
http://localhost:3000
```
**The app by default listens to port 3000. To change it to any other port update the listener in the the app.js file and restart.**

#How to use Pewter
Using **Pewter** is extremely simple. Follow the annotations on the images below and you will be able to kick off in a few minutes.
###Data Acquisition<br/>
The following are the functions of the buttons available,<br/>
1. **Play**: Starts recording data.<br/>
2. **Pause**: Pauses recording data.<br/>
3. **Undo**: Undos the recording.<br/>
4. **save**: Saves the experiment data.<br/>
5. **Visualizations****: Redirects to the visualization page.<br/>

***Please give an 'Experiment Name' before saving data.***
        
![alt tag](https://sigvoiced.files.wordpress.com/2016/07/screenshot-51.png)

####Where is the data saved?
The data is saved inside the '**experimentdata**' directory inside the root directory of the project.

####What is the data format?
The data is saved in json format. The following is the structure of a sample experiment data.

```json
{
  "expName": "test",
  "emg": {
    "data": [
      [
        13,
        11,
        5,
        2,
        22,
        10,
        3,
        5
      ]
    ],
    "timestamps": [
      "1468000525763185"
    ]
  },
  "gyr": {
    "data": [
      [
        -0.75,
        -0.375,
        2.0625
      ]
    ],
    "timestamps": [
      "1468000525755180"
    ]
  },
  "ori": {
    "data": [
      [
        0.48699951171875,
        -0.339599609375,
        -0.69305419921875,
        0.408935546875
      ]
    ],
    "timestamps": [
      "1468000525755180"
    ]
  },
  "acc": {
    "data": [
      [
        -0.39404296875,
        0.8837890625,
        0.291015625
      ]
    ],
    "timestamps": [
      "1468000525755180"
    ]
  }
}
```
<br/>

#####For EMG

Key | Value (Data from sensor)
--- | --- 
emg.data[0][0] | EMG POD 0
emg.data[0][1] | EMG POD 1
emg.data[0][2] | EMG POD 2
emg.data[0][3] | EMG POD 3
emg.data[0][4] | EMG POD 4
emg.data[0][5] | EMG POD 5
emg.data[0][6] | EMG POD 6
emg.data[0][7] | EMG POD 7
emg.timestamps[0] | Timestamp for emg.data[0]

#####For Accelerometer

Key | Value 
--- | --- 
acc.data[0][0] | Accelerometer_x
acc.data[0][1] | Accelerometer_y
acc.data[0][2] | Accelerometer_z
acc.timestamps[0] | Timestamp for acc.data[0]

#####For Gyroscope

Key | Value 
--- | --- 
gyr.data[0][0] | Gyroscope_x
gyr.data[0][1] | Gyroscope_y
gyr.data[0][2] | Gyroscope_z
gyr.timestamps[0] | Timestamp for gyr.data[0]

#####For Orientation

Key | Value 
--- | --- 
ori.data[0][0] | Orientation_x
ori.data[0][1] | Orientation_y
ori.data[0][2] | Orientation_z
ori.data[0][3] | Orientation_w
ori.timestamps[0] | Timestamp for ori.data[0]

###Visualisation




