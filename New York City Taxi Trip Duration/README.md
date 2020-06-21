# New York Taxi Trip Duration prediction

The competition dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC). The data was sampled and cleaned for the purposes of this playground competition. Based on individual trip attributes, participants should predict the duration of each trip in the test set.

# Data

train.csv - the training set (contains 1458644 trip records)
test.csv - the testing set (contains 625134 trip records)

## Fields

1. id - a unique identifier for each trip
2. vendor_id - a code indicating the provider associated with the trip record
3. pickup_datetime - date and time when the meter was engaged
4. dropoff_datetime - date and time when the meter was disengaged
5. passenger_count - the number of passengers in the vehicle (driver entered value)
6. pickup_longitude - the longitude where the meter was engaged
7. pickup_latitude - the latitude where the meter was engaged
8. dropoff_longitude - the longitude where the meter was disengaged
9. dropoff_latitude - the latitude where the meter was disengaged
10. store_and_fwd_flag - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor 11. because the vehicle did not have a connection to the server - Y=store and forward; N=not a store and forward trip
12. trip_duration - duration of the trip in seconds

Disclaimer: The decision was made to not remove dropoff coordinates from the dataset order to provide an expanded set of variables to use in Kernels.

# Evaluation
The evaluation metric for this competition is Root Mean Squared Logarithmic Error.

The RMSLE is calculated as

\epsilon = \sqrt{\frac{1}{n} \sum_{i=1}^n (\log(p_i + 1) - \log(a_i+1))^2 }

Where:

ϵ is the RMSLE value (score)
n is the total number of observations in the (public/private) data set,
pi is your prediction of trip duration, and
ai is the actual trip duration for i.
log(x) is the natural logarithm of x

## Acknowledgments

* https://www.kaggle.com/c/nyc-taxi-trip-duration/overview/evaluation
