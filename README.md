# Conversions API for Offline Events Python Script

This python script is an example on how you can upload your offline events via Meta Conversions API for Offline. This is just a sample script and you can modify ths as per your use case.

## Prerequisites

### Config file

You need to udpate the config file with your config details which are need to make CAPI for Offline Calls. Below are all the sections and what needs to be in there.

> Don't use single or double quotes in this fike

#### dataset Section

You need to set your DATASET ID, API Version and Access Token here.

#### offline_events_file section

Specify the path to the offline events CSV file

#### user_data section

Here you need to specify the user data columns that you will be sending. For example if you plan to send email and phone number, it will look something like this. The value can be null. It will be read from the CSV file

```
[user_data]
em = null #EMAIL
ph = null #PHONE NUMBER
```

If your CSV fill have email, phone and First Name, then

```
[user_data]
em = null #EMAIL
ph = null #PHONE NUMBER
fn = null # First Name
```

whatever fields you specify here needs to be present in the CSV file and the column name should be same as the key here. For exanple em, ph. Below is all the user data you can send and their field names

```
[user_data]
em = null #EMAIL
ph = null #PHONE NUMBER
fn = null # First Name
ln = null # Last Name
ge = null # Gender
db = null # Date of Birth
ct = null # City
st = null # State
zp = null # Zip Code
country = null # Country
```

#### optional_offline_custom_data section

Here you can specify all the optional custom data field you wish to send. Refer to the [developer doc](https://developers.facebook.com/docs/marketing-api/conversions-api/offline-events#custom-data-parameters) for all required and optional colum names.

For example, if you want to send content_type and contents, it will look like this. The value can be null. It will be read from the CSV file

```
[optional_offline_custom_data]
content_type = null
contents = null
```

whatever fields you specify here needs to be present in the CSV file and the column name should be same as the key here. Below is a list of all fields that you can add

```
[optional_offline_custom_data]
content_type = null
contents = null
custom_data = null
order_id = null
item_number = null
```

Refer to the link above to check what each of the fields mean.


#### log_file Section

Specify where you want the log file and a file name

### Offline Event CSV Export

You will need a csv file with your offline events. The column names will need to be in a specific format for this script to run correctly.

#### Required and Optional Columns

Refer to the [developer doc](https://developers.facebook.com/docs/marketing-api/conversions-api/offline-events#custom-data-parameters) for all required and optional colum names.

> Note that the column name in the CSV file must be *EXACTLY* same as shown in above developer page.

List of required fields are

* event_time
* event_name
* currency
* value

Refer to the link above to check what each of the fields mean.


#### User data

Refer to the *user_data* section to check what columns you need to send any user data

#### Custom data

Refer to the *optional_offline_custom_data section* section to check what columns you need to send any custom data


#### Sample CSV file

```
em,ph,event_time,event_name,currency,value,order_id,content_type,contents,execution_id
johndoe@gmail.com,12312,1695919455,Purchase,USD,20,BusinessDate=2023-06-01&StationId=1&StoreId=1188&TransactionId=7208,product,"[{ id: ""810547695"", quantity: 1, price: 11.9900 }, { id: ""810409941"", quantity: 1, price: 3.9900 }]",1.69E+12
maryjane@gmail.com,12312,1695919555,Purchase,USD,40,BusinessDate=2023-06-01&StationId=1&StoreId=1188&TransactionId=7208,product,"[{ id: ""810547695"", quantity: 1, price: 11.9900 }, { id: ""810409941"", quantity: 1, price: 3.9900 }]",1.69E+12
harveyspectre@gmail.com,12312,1695919655,Purchase,USD,60,BusinessDate=2023-06-01&StationId=1&StoreId=1188&TransactionId=7208,product,"[{ id: ""810547695"", quantity: 1, price: 11.9900 }, { id: ""810409941"", quantity: 1, price: 3.9900 }]",1.69E+12
```


### How to run the script

```
python3 offline_CAPI.py
```

You can check the log file set in the log_file section.
