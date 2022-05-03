# Alto ML Code Test v1.0

## _Data_
The datasets provided with this code test are a representative small sample of our passenger booking and engagement behaviors and experiences. The sections below outline details about the included files and provide general guidance for usage of this data, but it should be noted that you are not restricted to using solely information included in this dataset. If there are external data sources or factors that you believe could be included, feel free to use those as part of your exercise.

### _Passengers_
The Passenger dataset is a subsample of passengers that registered in a similar timeframe. Customers included in this dataset are only selected based on their registration date and no other filters or selection criteria have been applied to further segment who is included.


| Field Name | Data Type | Description |
| ---------- | --------- | ----------- |
| passenger_guid | uuid | Unique identifier for a customer used to link data across datasets| 
| passenger_created_date | date | Date the passenger registered with Alto |


### _Passenger Engagements_
The Passenger Engagements dataset is a time series sample of passenger engagements (defined as non-booking events either in our apps or other systems) for the selected sample of customers used for the basis of this test. These engagements can be interpreted as customer-led events (ex. interacting with their app that may not necessarily be a booking, but can also be inclusive of booking attempts) that are indicative of customer engagement with our service. It should be noted that engagements included in this dataset may or may not be positive and may be indicative of errors or other negative experiences that could impact a customer’s perception and future usage of Alto.

| Field Name | Data Type | Description |
| ---------- | --------- | ----------- |
| passenger_guid | uuid | Unique identifier for a customer used to link data across datasets |
| event_date | date | Date on which a passenger had an engagement event recorded in our system |
| customer_engagements | numeric | Sum total of customer engagement events record for a give customer for a given date|


### _Completed Bookings_
The Completed Bookings dataset is a time series sample of passenger bookings that were successfully carried out and resulted in the passenger being taken to their requested destination. Passengers may or may not book consistently, so interpret customer behaviors based on the data you have available to you across all datasets.

| Field Name | Data Type | Description |
| ---------- | --------- | ----------- |
| booking_date | date | Date on which a passenger had a successfully completed booking with Alto |
| passenger_guid | uuid | Unique identifier for a customer used to link data across datasets |
| completed_bookings | numeric | Sum total of completed bookings for a given customer on a given date |


### _NVA Bookings_
The NVA Bookings dataset is a sample of time series passenger bookings that were requested, but were unable to be fulfilled and resulted in the passenger NOT being taken to their requested destination. We call this occurrence a “no vehicles available” or NVA. Passengers may or may not have eventually successfully booked with Alto and been taken to their destination and passengers can potentially have a number of NVAs in attempting to get a successful booking. This is usually a negative experience for our customers, but their behaviors after receiving one or more NVAs varies greatly.

| Field Name | Data Type | Description |
| ---------- | --------- | ----------- |
| booking_date | date | Date on which a passenger had an unsuccessful booking request with Alto |
| passenger_guid | uuid | Unique identifier for a customer used to link data across datasets |
| nva_bookings | numeric | Sum total of no vehicle available bookings for a given customer on a given date |