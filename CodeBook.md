# Analysis of Human Activity Recognition - Using Smartphone Data

## Data Source:
Jorge L. Reyes-Ortiz(1,2), Davide Anguita(1), Alessandro Ghio(1), Luca Oneto(1) and Xavier Parra(2)
1 - Smartlab - Non-Linear Complex Systems Laboratory DITEN - Università degli Studi di Genova, Genoa (I-16145), Italy.
2 - CETpD - Technical Research Centre for Dependency Care and Autonomous Living
Universitat Politècnica de Catalunya (BarcelonaTech). Vilanova i la Geltrú (08800), Spain

For more information on the data source check out the [U.C. Irvine Center for Machine Learning and Intelligent Systems](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) or contact: "activityrecognition@smartlab.ws"

## Summary:

The purpose of this project is to demonstrate collecting, working with, and cleaning a data set. The goal is to prepare tidy data from smartphone data to be used for later analysis.  The data was captured from the embedded accelerometer and gyroscope on smartphones from 30 volunteers within an age bracket of 19-48 years that performed six activities. The obtained data was randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details.

### The [dataset](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) includes the following files:

- 'README.txt'
- 'features_info.txt': Shows information about the variables used on the feature vector.
- 'features.txt': List of all features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.

### Feature Selection  (features_info.txt)
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag).

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for each pattern:
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

### Notes:
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.

For more information about this dataset contact: activityrecognition@smartlab.ws

### Data Dictionary for tidy data set from Step 5.

Note that the summary consists of the average of the standard deviations and means for the combined test and training data, with unit of hertz.

<table cellspacing="0" border="0">
	<colgroup width="30"></colgroup>
	<colgroup width="207"></colgroup>
	<colgroup width="586"></colgroup>
	<tr>
		<td height="19" align="right" valign=bottom sdval="1" sdnum="1033;">1</td>
		<td align="left" valign=bottom>subject</td>
		<td align="left" valign=bottom>Subject who carried out the experiment</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="2" sdnum="1033;">2</td>
		<td align="left" valign=bottom>activity</td>
		<td align="left" valign=bottom sdnum="1033;0;0.00%">Activity carried out by subject</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="3" sdnum="1033;">3</td>
		<td align="left" valign=bottom>tBodyAccmeanX</td>
		<td align="left" valign=bottom sdnum="1033;0;0.00%">mean of the body accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="4" sdnum="1033;">4</td>
		<td align="left" valign=bottom>tBodyAccmeanY</td>
		<td align="left" valign=bottom sdnum="1033;0;0.00%">mean of the body accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="5" sdnum="1033;">5</td>
		<td align="left" valign=bottom>tBodyAccmeanZ</td>
		<td align="left" valign=bottom sdnum="1033;0;0.00%">mean of the body accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="6" sdnum="1033;">6</td>
		<td align="left" valign=bottom>tBodyAccstdX</td>
		<td align="left" valign=bottom>standard deviation of the body accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="7" sdnum="1033;">7</td>
		<td align="left" valign=bottom>tBodyAccstdY</td>
		<td align="left" valign=bottom>standard deviation of the body accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="8" sdnum="1033;">8</td>
		<td align="left" valign=bottom>tBodyAccstdZ</td>
		<td align="left" valign=bottom>standard deviation of the body accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="9" sdnum="1033;">9</td>
		<td align="left" valign=bottom>tGravityAccmeanX</td>
		<td align="left" valign=bottom>mean of the gravity accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="10" sdnum="1033;">10</td>
		<td align="left" valign=bottom>tGravityAccmeanY</td>
		<td align="left" valign=bottom>mean of the gravity accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="11" sdnum="1033;">11</td>
		<td align="left" valign=bottom>tGravityAccmeanZ</td>
		<td align="left" valign=bottom>mean of the gravity accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="12" sdnum="1033;">12</td>
		<td align="left" valign=bottom>tGravityAccstdX</td>
		<td align="left" valign=bottom>standard deviation of the gravity accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="13" sdnum="1033;">13</td>
		<td align="left" valign=bottom>tGravityAccstdY</td>
		<td align="left" valign=bottom>standard deviation of the gravity accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="14" sdnum="1033;">14</td>
		<td align="left" valign=bottom>tGravityAccstdZ</td>
		<td align="left" valign=bottom>standard deviation of the gravity accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="15" sdnum="1033;">15</td>
		<td align="left" valign=bottom>tBodyAccJerkmeanX</td>
		<td align="left" valign=bottom>mean of the body jerk accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="16" sdnum="1033;">16</td>
		<td align="left" valign=bottom>tBodyAccJerkmeanY</td>
		<td align="left" valign=bottom>mean of the body jerk accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="17" sdnum="1033;">17</td>
		<td align="left" valign=bottom>tBodyAccJerkmeanZ</td>
		<td align="left" valign=bottom>mean of the body jerk accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="18" sdnum="1033;">18</td>
		<td align="left" valign=bottom>tBodyAccJerkstdX</td>
		<td align="left" valign=bottom>standard deviation of the body jerk accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="19" sdnum="1033;">19</td>
		<td align="left" valign=bottom>tBodyAccJerkstdY</td>
		<td align="left" valign=bottom>standard deviation of the body jerk accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="20" sdnum="1033;">20</td>
		<td align="left" valign=bottom>tBodyAccJerkstdZ</td>
		<td align="left" valign=bottom>standard deviation of the body jerk accelerometer raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="21" sdnum="1033;">21</td>
		<td align="left" valign=bottom>tBodyGyromeanX</td>
		<td align="left" valign=bottom>mean of the body gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="22" sdnum="1033;">22</td>
		<td align="left" valign=bottom>tBodyGyromeanY</td>
		<td align="left" valign=bottom>mean of the body gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="23" sdnum="1033;">23</td>
		<td align="left" valign=bottom>tBodyGyromeanZ</td>
		<td align="left" valign=bottom>mean of the body gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="24" sdnum="1033;">24</td>
		<td align="left" valign=bottom>tBodyGyrostdX</td>
		<td align="left" valign=bottom>standard deviation of the body gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="25" sdnum="1033;">25</td>
		<td align="left" valign=bottom>tBodyGyrostdY</td>
		<td align="left" valign=bottom>standard deviation of the body gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="26" sdnum="1033;">26</td>
		<td align="left" valign=bottom>tBodyGyrostdZ</td>
		<td align="left" valign=bottom>standard deviation of the body gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="27" sdnum="1033;">27</td>
		<td align="left" valign=bottom>tBodyGyroJerkmeanX</td>
		<td align="left" valign=bottom>mean of the body jerk gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="28" sdnum="1033;">28</td>
		<td align="left" valign=bottom>tBodyGyroJerkmeanY</td>
		<td align="left" valign=bottom>mean of the body jerk gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="29" sdnum="1033;">29</td>
		<td align="left" valign=bottom>tBodyGyroJerkmeanZ</td>
		<td align="left" valign=bottom>mean of the body jerk gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="30" sdnum="1033;">30</td>
		<td align="left" valign=bottom>tBodyGyroJerkstdX</td>
		<td align="left" valign=bottom>standard deviation of the body jerk gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="31" sdnum="1033;">31</td>
		<td align="left" valign=bottom>tBodyGyroJerkstdY</td>
		<td align="left" valign=bottom>standard deviation of the body jerk gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="32" sdnum="1033;">32</td>
		<td align="left" valign=bottom>tBodyGyroJerkstdZ</td>
		<td align="left" valign=bottom>standard deviation of the body jerk gyroscope raw time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="33" sdnum="1033;">33</td>
		<td align="left" valign=bottom>tBodyAccMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body accelerometer time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="34" sdnum="1033;">34</td>
		<td align="left" valign=bottom>tBodyAccMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body accelerometer time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="35" sdnum="1033;">35</td>
		<td align="left" valign=bottom>tGravityAccMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude gravity accelerometer time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="36" sdnum="1033;">36</td>
		<td align="left" valign=bottom>tGravityAccMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude gravity accelerometer time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="37" sdnum="1033;">37</td>
		<td align="left" valign=bottom>tBodyAccJerkMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body jerk accelerometer time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="38" sdnum="1033;">38</td>
		<td align="left" valign=bottom>tBodyAccJerkMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body jerk accelerometer time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="39" sdnum="1033;">39</td>
		<td align="left" valign=bottom>tBodyGyroMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body gyroscope time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="40" sdnum="1033;">40</td>
		<td align="left" valign=bottom>tBodyGyroMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body gyroscope time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="41" sdnum="1033;">41</td>
		<td align="left" valign=bottom>tBodyGyroJerkMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body jerk gyroscope time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="42" sdnum="1033;">42</td>
		<td align="left" valign=bottom>tBodyGyroJerkMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body jerk gyroscope time domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="43" sdnum="1033;">43</td>
		<td align="left" valign=bottom>fBodyAccmeanX</td>
		<td align="left" valign=bottom>mean of the body accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="44" sdnum="1033;">44</td>
		<td align="left" valign=bottom>fBodyAccmeanY</td>
		<td align="left" valign=bottom>mean of the body accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="45" sdnum="1033;">45</td>
		<td align="left" valign=bottom>fBodyAccmeanZ</td>
		<td align="left" valign=bottom>mean of the body accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="46" sdnum="1033;">46</td>
		<td align="left" valign=bottom>fBodyAccstdX</td>
		<td align="left" valign=bottom>standard deviation of the body accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="47" sdnum="1033;">47</td>
		<td align="left" valign=bottom>fBodyAccstdY</td>
		<td align="left" valign=bottom>standard deviation of the body accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="48" sdnum="1033;">48</td>
		<td align="left" valign=bottom>fBodyAccstdZ</td>
		<td align="left" valign=bottom>standard deviation of the body accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="49" sdnum="1033;">49</td>
		<td align="left" valign=bottom>fBodyAccJerkmeanX</td>
		<td align="left" valign=bottom>mean of the body jerk accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="50" sdnum="1033;">50</td>
		<td align="left" valign=bottom>fBodyAccJerkmeanY</td>
		<td align="left" valign=bottom>mean of the body jerk accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="51" sdnum="1033;">51</td>
		<td align="left" valign=bottom>fBodyAccJerkmeanZ</td>
		<td align="left" valign=bottom>mean of the body jerk accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="52" sdnum="1033;">52</td>
		<td align="left" valign=bottom>fBodyAccJerkstdX</td>
		<td align="left" valign=bottom>standard deviation of the body jerk accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="53" sdnum="1033;">53</td>
		<td align="left" valign=bottom>fBodyAccJerkstdY</td>
		<td align="left" valign=bottom>standard deviation of the body jerk accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="54" sdnum="1033;">54</td>
		<td align="left" valign=bottom>fBodyAccJerkstdZ</td>
		<td align="left" valign=bottom>standard deviation of the body jerk accelerometer raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="55" sdnum="1033;">55</td>
		<td align="left" valign=bottom>fBodyGyromeanX</td>
		<td align="left" valign=bottom>mean of the body gyroscope raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="56" sdnum="1033;">56</td>
		<td align="left" valign=bottom>fBodyGyromeanY</td>
		<td align="left" valign=bottom>mean of the body gyroscope raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="57" sdnum="1033;">57</td>
		<td align="left" valign=bottom>fBodyGyromeanZ</td>
		<td align="left" valign=bottom>mean of the body gyroscope raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="58" sdnum="1033;">58</td>
		<td align="left" valign=bottom>fBodyGyrostdX</td>
		<td align="left" valign=bottom>standard deviation of the body gyroscope raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="59" sdnum="1033;">59</td>
		<td align="left" valign=bottom>fBodyGyrostdY</td>
		<td align="left" valign=bottom>standard deviation of the body gyroscope raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="60" sdnum="1033;">60</td>
		<td align="left" valign=bottom>fBodyGyrostdZ</td>
		<td align="left" valign=bottom>standard deviation of the body gyroscope raw frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="61" sdnum="1033;">61</td>
		<td align="left" valign=bottom>fBodyAccMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body accelerometer frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="62" sdnum="1033;">62</td>
		<td align="left" valign=bottom>fBodyAccMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body accelerometer frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="63" sdnum="1033;">63</td>
		<td align="left" valign=bottom>fBodyBodyAccJerkMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body jerk accelerometer frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="64" sdnum="1033;">64</td>
		<td align="left" valign=bottom>fBodyBodyAccJerkMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body jerk accelerometer frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="65" sdnum="1033;">65</td>
		<td align="left" valign=bottom>fBodyBodyGyroMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body gyroscope frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="66" sdnum="1033;">66</td>
		<td align="left" valign=bottom>fBodyBodyGyroMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body gyroscope frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="67" sdnum="1033;">67</td>
		<td align="left" valign=bottom>fBodyBodyGyroJerkMagmean</td>
		<td align="left" valign=bottom>mean of the magnitude body jerk gyroscope frequency domain signals</td>
	</tr>
	<tr>
		<td height="19" align="right" valign=bottom sdval="68" sdnum="1033;">68</td>
		<td align="left" valign=bottom>fBodyBodyGyroJerkMagstd</td>
		<td align="left" valign=bottom>standard deviation of the magnitude body jerk gyroscope frequency domain signals</td>
	</tr>
</table>

