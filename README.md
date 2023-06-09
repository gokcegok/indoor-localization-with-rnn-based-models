# INDOOR LOCALIZATION/NAVIGATION WITH RNN, LSTM AND GRU

In this study, I compare RNN, LSTM and GRU methods for indoor localization/navigation with BLE RSSI readings. 

![Comparison](results.jpg)

## DATASET 

The dataset was created using the RSSI readings of an array of 13 iBeacons in the first floor of Waldo Library, Western Michigan University. Data was collected using iPhone 6S. The dataset contains two sub-datasets: a labeled dataset (1420 instances) and an unlabeled dataset (5191 instances). The recording was performed during the operational hours of the library. For the labeled dataset, the input data contains the location (label column), a timestamp, followed by RSSI readings of 13 iBeacons[1].

In the original dataset, locations are combinations of letters and numbers. Letters symbolize the x-axis and the numbers the y-axis. I translated the letters to numbers for using them like cartesian coordinates.

Before, the locations looked like A01, B05, I02 etc. I transformed this symbolization to like (0, 1), (1, 5), (8, 2) etc. So, I treated the problem as a regression problem and tried to solve it from that perspective.

## PERFORMANCE METRICS

As I mentioned, I generate x and y cartesian coordinates from the “location” feature. Therefore, I adapted the performance metrics to include a geometric perspective. I used Euclidean Distance for RMSE calculation and Manhattan Distance for MAE calculation. I calculated the MAPE separately in the x and y directions.

## REFERENCES

[1] M. Mohammadi, BLE RSSI Dataset for Indoor Localization and Navigation

[2] I. Alexander, G. P. Kusuma, "Predicting Indoor Position Using Bluetooth Low Energy and Machine Learning", International Journal of Scientific \& Technology Research Vol 8, 2019.

[3] S. Akleylek,, E. Kılıç,, B. Söylemez,, T.E. Aruk,, A. Çavuş Yıldırım,, "A Research On Indoor Positioning Systems", Journal of Engineering Sciences and Design, 8(5), 90-105	

[4] R. Ramirez,, C.-Y. Huang,, C.-A. Liao,, P.-T. Lin,, H.-W. Lin,, S.-H. Liang,, "A Practice of BLE RSSI Measurement for Indoor Positioning". Sensors 2021, 21, 5181. https://doi.org/10.3390/s21155181                     

[5] Z. Jianyong, L. Haiyong, C. Zili and L. Zhaohui, "RSSI based Bluetooth low energy indoor positioning," 2014 International Conference on Indoor Positioning and Indoor Navigation (IPIN), Busan, 2014, pp. 526-533, doi: 10.1109/IPIN.2014.7275525 

[6] C. Jain, G. V. S. Sashank, V. N and S. Markkandan, "Low-cost BLE based Indoor Localization using RSSI Fingerprinting and Machine Learning," 2021 Sixth International Conference on Wireless Communications, Signal Processing and Networking (WiSPNET), Chennai, India, 2021, pp. 363-367, doi: 10.1109/WiSPNET51692.2021.9419388
