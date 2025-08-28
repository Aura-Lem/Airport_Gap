## Context:
[auth_errors_rep_001](#auth_errors_rep_001)  
[get_details_rep_002](#get_details_rep_002) 
[get_errors_rep_003](#get_errors_rep_003) 
[calculate_dist_rep_004](#calculate_dist_rep_004) 
[calculate_dist_errors_rep_005](#calculate_dist_errors_rep_005) 
[favorites_details_rep_006](#favorites_details_rep_006) 
[favorites_details_note_rep_007](#favorites_details_note_rep_007) 
[favorites_errors_rep_008](#favorites_errors_rep_008) 
[update_favorites_details_rep_009](#update_favorites_details_rep_009) 


### auth_errors_rep_001:
[back](#context)
```json
{
    "errors": [
        {
            "status": "401",
            "title": "Unauthorized",
            "detail": "You are not authorized to perform the requested action."
        }
    ]
}
```
### get_details_rep_002:
[back](#context)
```json
{
    "data": {
        "id": "GKA",
        "type": "airport",
        "attributes": {
            "name": "Goroka Airport",
            "city": "Goroka",
            "country": "Papua New Guinea",
            "iata": "GKA",
            "icao": "AYGA",
            "latitude": "-6.08169",
            "longitude": "145.391998",
            "altitude": 5282,
            "timezone": "Pacific/Port_Moresby"
        }
    }
}
```
### get_errors_rep_003:
[back](#context)
```json
{
    "errors": [
        {
            "status": "404",
            "title": "Not Found",
            "detail": "The page you requested could not be found"
        }
    ]
}
```
### calculate_dist_rep_004:
[back](#context)
```json
{
    "data": {
        "id": "GKA-KIX",
        "type": "airport_distance",
        "attributes": {
            "from_airport": {
                "id": 1,
                "name": "Goroka Airport",
                "city": "Goroka",
                "country": "Papua New Guinea",
                "iata": "GKA",
                "icao": "AYGA",
                "latitude": "-6.08169",
                "longitude": "145.391998",
                "altitude": 5282,
                "timezone": "Pacific/Port_Moresby"
            },
            "to_airport": {
                "id": 3158,
                "name": "Kansai International Airport",
                "city": "Osaka",
                "country": "Japan",
                "iata": "KIX",
                "icao": "RJBB",
                "latitude": "34.427299",
                "longitude": "135.244003",
                "altitude": 26,
                "timezone": "Asia/Tokyo"
            },
            "kilometers": 4628.82980331026,
            "miles": 2874.219228048248,
            "nautical_miles": 2497.627025190087
        }
    }
}
```
### calculate_dist_errors_rep_005:
[back](#context)
```json
{
    "errors": [
        {
            "status": "422",
            "title": "Unable to process request",
            "detail": "Please enter valid 'from' and 'to' airports."
        }
    ]
}
```
### favorites_details_rep_006:
[back](#context)
```json
{
    "data": {
        "id": "37540",
        "type": "favorite",
        "attributes": {
            "airport": {
                "id": 14,
                "name": "Húsavík Airport",
                "city": "Husavik",
                "country": "Iceland",
                "iata": "HZK",
                "icao": "BIHU",
                "latitude": "65.952301",
                "longitude": "-17.426001",
                "altitude": 48,
                "timezone": "Atlantic/Reykjavik"
            },
            "note": null
        }
    }
}
```
### favorites_details_note_rep_007:
[back](#context)
```json
{
    "data": {
        "id": "37541",
        "type": "favorite",
        "attributes": {
            "airport": {
                "id": 16,
                "name": "Keflavik International Airport",
                "city": "Keflavik",
                "country": "Iceland",
                "iata": "KEF",
                "icao": "BIKF",
                "latitude": "63.985001",
                "longitude": "-22.6056",
                "altitude": 171,
                "timezone": "Atlantic/Reykjavik"
            },
            "note": "The Best"
        }
    }
}
```
### favorites_errors_rep_008:
[back](#context)
```json
{
    "errors": [
        {
            "status": "422",
            "title": "Unable to process request",
            "detail": "Airport Please enter a valid airport code"
        }
    ]
}
```
### update_favorites_details_rep_009:
[back](#context)
```json
{
    "data": {
        "id": "37540",
        "type": "favorite",
        "attributes": {
            "airport": {
                "id": 14,
                "name": "Húsavík Airport",
                "city": "Husavik",
                "country": "Iceland",
                "iata": "HZK",
                "icao": "BIHU",
                "latitude": "65.952301",
                "longitude": "-17.426001",
                "altitude": 48,
                "timezone": "Atlantic/Reykjavik"
            },
            "note": "good one"
        }
    }
}
```

