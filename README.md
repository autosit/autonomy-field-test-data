# autonomy-field-test-data

## Data explanation

The data depicted in the figures in the related paper is found in the data folder. The files are numbered according to their order in the paper.

The data is contained in .npz files, and each file contains the following lists:
- radar_measurements
- ais_measurements 
- ownship
- estimates
- ground_truth

The different lists are structured in the following ways:

### radar_measurements
Contains the radar measurements, and is a list of measurements for each scan. The individual measurements are contained in dicts with the following fields:
- x_pos: x-position relative to origo
- y_pos: y-position relative to origo
- timestamp: UTC time

### ais_measurements
Contains the AIS measurements, and is a list of measurements for each time they arrive. The individual measurements are contained in dicts with the following fields:
- x_pos: x-position relative to origo
- y_pos: y-position relative to origo
- timestamp: UTC time
- mmsi: MMSI number (ID)
- course
- speed

### ownship
Contains the radar measurements, and is a dict for each time a radar scan has been received. The individual states are contained in dicts with the following fields:
- x_pos: x-position relative to origo
- y_pos: y-position relative to origo
- timestamp: UTC time
- course
- speed


### estimates
Contains the estimates output from the tracker, and is a list of tracks estimated at each radar time stamp. The individual estimates are contained in dicts with the following fields:
- x_pos: x-position relative to origo
- y_pos: y-position relative to origo
- timestamp: UTC time
- speed
- speed_std_dev: standard deviation of the speed estimate
- course
- course_std_dev: standard deviation of the course estimate

### ground_truth
Contains the gps positions of the targets, and is a list of lists, where each nested list conatins the received positions of one target. The individual positions are contained in dicts with the following fields:
- x_pos: x-position relative to origo
- y_pos: y-position relative to origo
- timestamp: UTC time

The data is protected under the CC BY-NC 4.0 license.
