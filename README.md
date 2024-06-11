# Wi-Fi Handwashing Integrity Tracking and Evaluation

We have created a dataset used for wifi-based activity recognition.
There are two volunteers, A and B. They perform handwashing motions in a designated area. We used two Raspberry Pis to collect WiFi CSI data during that period. We track 12 different motion types. According to the World Health Organization (WHO) guidelines, five hand-washing motions are required for each hand, totaling 10. We also include two additional cases - one where the space is empty without any hands present and another where hands are present but not moving. This gives us 12 different labels for multi-class classification. The CSI data's shape is (2600, 64, 1500). The first dimension (2600) is the number of data samples. The second dimension (64) is the count of OFDM subcarriers. We collected data for around 7.5 seconds for each sample, which is the WHO-recommended duration for each motion on each hand, and that equates to (1500) samples in each time series. Each time series is recorded as a pcap file containing the CSI values as complex numbers.

We provide a sample dataset containing the static hands.
For more details and the complete dataset, please contact me at - 

<email: mritunjay.peelam@pilani.bits-pilani.ac.in>
