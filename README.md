# reverse-geocode
Salesforce trigger and classes for a reverse geocode lookup on a geolocation field in a Salesforce quote to populate the address using Opencage Geocoder and Rapid API.

In order to use this code, you will need to set up an account with Rapid API at http://www.rapidapi.com and OpenCage Geocoder at https://opencagedata.com/. This API allows for up to 2,500 calls/day for free. The code can easily be modified to work with another API that does reverse geolocation. You can find some othe roptions here: https://geoservices.tamu.edu/Services/Geocode/OtherGeocoders/.

This code was built to trigger from a custom geolocation field on the Quote object and populate custom Address fields. However, it can easily be modified to work with any custom/standard object and fields in Salesforce.

Because of the limitations of the geolocation API I chose, this code makes an API call for EACH record that is updated. If you need to make bulk API calls because of your Salesforce API limitations, you will need to modify the code to make the request in bulk and work with an API that will accept bulk requests.
