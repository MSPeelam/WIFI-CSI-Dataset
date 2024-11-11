# Wi-Fi Handwashing Integrity Tracking and Evaluation

### Introduction
We have created a WiFi CSI based dataset that can be used for handwashing or hand-rubbing motion detection. These motions are according to the World Health Organization (WHO) surgical hands preparation guidelines ([link for WHO guide](https://www.who.int/publications/i/item/9789241597906)).

### Data Collection
We request 55 volunteers, to perform handwashing motions in a designated area and use a Raspberry Pi to collect WiFi CSI data during that period. We collect data using Raspberry pi using the nexmon library - ([Nexmon Library link](https://github.com/seemoo-lab/nexmon)).
The volunteers perform 12 different types of hand-rubbing motion. There are five hand-rubbing motions described in the WHO guide for each hand, totaling 10 motions. We also include two additional cases - one where the space is empty without any hands present and another where hands are present in the experimental space but are not moving, thus a sum total of 12 motions. This gives us 12 different labels for multi-class classification.

### Data Format
Each hand-rubbing CSI data time series is recorded as a pcap file containing the CSI values as complex numbers, and that has to be converted to CSV format and the complex values are converted to the amplitude and phase form using this library - ([link](https://github.com/cheeseBG/pcap-to-csv)).

### Data Dimensions
The CSI final data is in CSV format and the shape of the data is (2600, 64, 1500, 2). The first dimension (2600) is the number of data samples. The second dimension (64) is the count of OFDM subcarriers. We collected data for around 7.5 seconds for each sample, which is the WHO-recommended duration for each motion on each hand, and that equates to (1500) samples in each time series. The fourth dimension (2) is the amplitude and phase of the data point.


We provide a sample dataset containing the static hands.
For more details and the complete dataset, please contact me at - 
[amgone786@gmail.com](mailto:amgone786@gmail.com)
