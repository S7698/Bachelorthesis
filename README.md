# Bachelorthesis
Repository of all relevant coding

test
This is the main part of the script, which iterates over each subject, sensor, and axis. It processes the data files for each combination, calculates the Freeze Index, compares detected events with ground truth events, and calculates performance metrics such as sensitivity and specificity. The results are printed out for each axis and sensor and summarised at the end.

xcount
This function compares the ground truth (gtframe) and detected events (lframe), taking into account the delays (offDelay and onDelay). It returns the counts of true positives (TP), true negatives (TN), false positives (FP), false negatives (FN), and the number of events in the ground truth data.

xfi
This function calculates the Freeze Index (FI) for the input data, which is a measure used to detect freezing events based on frequency analysis. It returns the sum of the power in the locomotion and freeze bands, the Freeze Index, and the corresponding time points.
To achieve this, the frequency resolution of the Fast Fourier Transform (FFT) is calculated, which is the spacing between frequency bins in the FFT output. Calculating the integral of the power spectral density (PSD) over the local motion band and over the freeze band, allows to calculate the ratio of the freeze band area to the local motion band area, which is the Freeze Index.

plots
This function is used to visualise the collected data from one participant, by showing the accelerometer data for the three sensors and the three axes.

compare_lists
This function compares the detected events (llabels) with ground truth events (gtlabels). It checks if the intervals overlap and if the start time difference is within 10 units. If conditions are met, it records the detection and calculates the delay.

Delay_plot
This function is used to visualise the FOG events and their detection. to showcase the delay between both. For additional context the freeze index was included.
