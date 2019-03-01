# Reduce-Noise-in-LiDAR-sensor
[![build status of master](https://travis-ci.org/Svaity/Reduce-Noise-in-LiDAR-sensor.svg?branch=master)](https://travis-ci.org/Svaity/Reduce-Noise-in-LiDAR-sensor)

You have been assigned to write filters to reduce noise in the data coming from a LIDAR sensor attached
to your robot. The LIDAR generates scans at a certain rate. Each scan is an array of length N of lloat
values representing distance measurements. Nis typically in a range of ~[2Dl]. 1000] measurements, and
it is ﬁxed. Measured distances are typically in a range of [0.03, 5D] meters. Each time a scan is received.
it will be passed on to the filters. Each ﬁlter object should have an update method, that takes a length-N
array of ranges and retums a ﬁltered length-N array ot ranges.

We want you to write two different ﬁlter objects:
a A range ﬁlter

The range filter crops all the values that are below range_min (resp. above range_max), and
replaces them with the range_min value (resp. range_max)

. A temporal median ﬁlter
The temporal median ﬁlter returns the median of the current and the previous D scans:
}' Em =median(x.(r), 116— 1), . xfcx — DJ)
where x and y are input and output length—N scans and i ranges from D to N—1. The number of
previous scans D is a parameter that should be given when creating a new temporal median ﬁlter.
Note that, although the update method will receive a single scan, the retumed arrayr depends on
the values of previous scans. Note also that the for the first D scans, the ﬁlter is expected to

return the median of all the scans so far.
