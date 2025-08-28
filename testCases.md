### Testing API Airport Gap -> https://airportgap.com/

## Test Scenarios
``` 
TS 1. Authentication
TS 2. Get the airport.
TS 3. Calculate the distance.
TS 4. Save a favorite airport.
TS 5. Get the favorite airport by ID.
TS 6. Update the note of one of favorite airports.
TS 7. Delete one of favorite airports.
```

### Pre-requisites: 

1. Save base url: https://airportgap.com/api in Collection variables, named 'baseUrl'.

## TC 1.1 Positive Authenticate with email and password

#### Pre-requisites:
1. Get new token from https://airportgap.com/tokens/new with email and password.

Steps:
1. Add new POST request.
2. Add email and password in the body.
3. Write script and save token in collection variables.
4. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 200. 
> 2. Return token.    

## TC 1.2 Negative Authenticate with email and without password

Steps:
1. Add new POST request.
2. Add email in the body.
4. Click on button Send.

> 🎯 Expected result:  
>   1. Status code 401  
>   2. Located in file responseBodyResults with id auth_errors_rep_001 [link to auth_errors_rep_001](./responseBodyResults.md#auth_errors_rep_001)     

## TC 1.3 Negative Authenticate with password and without email

Steps:
1. Add new POST request.
2. Add password in the body.
4. Click on button Send.

> 🎯 Expected result: errors and status code 401.     
> 1. Status code 401.
> 2. Located in file responseBodyResults with id auth_errors_rep_001 [link to auth_errors_rep_001](./responseBodyResults.md#auth_errors_rep_001)

## TC 2.1. Positive Get the airport specified by the existing ID

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).

Steps:
1. Add new GET request.
2. Insert baseUrl and endpoint: '/airports/GKA'
3. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 200.  
> 2. Located in file responseBodyResults with id get_details_rep_002 [link to get_details_rep_002](./responseBodyResults.md#get_details_rep_002)   

## TC 2.2. Negative Get the airport specified by the not existing ID

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).

Steps:
1. Add new GET request.
2. Insert baseUrl and endpoint: '/airports/:id' with id MMM
3. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 404.  
> 2. Located in file responseBodyResults with id get_errors_rep_003 [link to get_errors_rep_003](./responseBodyResults.md#get_errors_rep_003)

## TC 3.1. Positive Calculate the distance between two airports with valid airport code

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).  

Steps:
1. Add new POST request.
2. Insert baseUrl and endpoint: '/airports/distance'.
3. Add key's in Query Params, named 'from' and 'to'.
4. Add values: the airport code (IATA location identifier) of the departure airport.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 200.  
> 2. Located in file responseBodyResults with id calculate_dist_rep_004 [link to calculate_dist_rep_004](./responseBodyResults.md#calculate_dist_rep_004)

## TC 3.2. Negative Calculate the distance between two airports without keys

Steps:
1. Add new POST request.
2. Insert baseUrl and endpoint: '/airports/distance'.
3. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 422.  
> 2. Located in file responseBodyResults with id calculate_dist_errors_rep_005 [link to calculate_dist_errors_rep_005](./responseBodyResults.md#calculate_dist_errors_rep_005)

## TC 3.3. Negative Calculate the distance between two airports with empty key 'from' value

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).  

Steps:
1. Add new POST request.
2. Insert baseUrl and endpoint: '/airports/distance'.
3. Add key's in Query Params, named 'from' and 'to'.
4. Add key 'to' value: the airport code (IATA location identifier) of the departure airport.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 422.  
> 2. Located in file responseBodyResults with id calculate_dist_errors_rep_005 [link to calculate_dist_errors_rep_005](./responseBodyResults.md#calculate_dist_errors_rep_005) 

## TC 3.4. Negative Calculate the distance between two airports with empty key 'to' value

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).  

Steps:
1. Add new POST request.
2. Insert baseUrl and endpoint: '/airports/distance'.
3. Add key's in Query Params, named 'from' and 'to'.
4. Add key 'from' value: the airport code (IATA location identifier) of the departure airport.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 422.  
> 2. Located in file responseBodyResults with id calculate_dist_errors_rep_005 [link to calculate_dist_errors_rep_005](./responseBodyResults.md#calculate_dist_errors_rep_005) 

## TC 3.5. Negative Calculate the distance between two airports with not existing ID

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).  

Steps:
1. Add new POST request.
2. Insert baseUrl and endpoint: '/airports/distance'.
3. Add key's in Query Params, named 'from' and 'to'.
4. Add key's value: from: valid, to: invalid.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 422.  
> 2. Located in file responseBodyResults with id calculate_dist_errors_rep_005 [link to calculate_dist_errors_rep_005](./responseBodyResults.md#calculate_dist_errors_rep_005)

## TC 4.1. Positive Save a favorite airport to Airport Gap account

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).

Steps:
1. Add new POST request.
2. Insert baseUrl'.
3. Select an authorization method Bearer token and enter token from collection variables.
4. Add Params 'airport_id' with Airport id value.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 201.  
> 2. Located in file responseBodyResults with id favorites_details_rep_006 [link to favorites_details_rep_006](./responseBodyResults.md#favorites_details_rep_006)

## TC 4.2. Positive Save a favorite airport to Airport Gap account with note

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).

Steps:
1. Add new POST request.
2. Insert baseUrl'.
3. Select an authorization method Bearer token and enter token from collection variables.
4. Add Params 'airport_id' with Airport id value.
5. Add in the Params note with message.
6. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 201.  
> 2. Located in file responseBodyResults with id favorites_details_note_rep_007 [link to favorites_details_note_rep_007](./responseBodyResults.md#favorites_details_note_rep_007) 

## TC 4.3. Negative Save a favorite airport to Airport Gap account with not existing Airport ID.

#### Pre-requisites: 
1. Get request with list of all airports details (endpoint: /airports).

Steps:
1. Add new POST request.
2. Insert baseUrl'.
3. Select an authorization method Bearer token and enter token from collection variables.
4. Add Params 'airport_id' with not existing Airport id value.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 422.  
> 2. Located in file responseBodyResults with id favorites_errors_rep_008 [link to favorites_errors_rep_008](./responseBodyResults.md#favorites_errors_rep_008) 

## TC 4.4. Negative Save a favorite airport to Airport Gap account without params info.

#### Pre-requisites:
1. Get request with list of all airports details (endpoint: /airports).

Steps:
1. Add new POST request.
2. Insert baseUrl'.
3. Select an authorization method Bearer token and enter token from collection variables.
4. Add Params 'airport_id' with empty value field.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 422.  
> 2. Located in file responseBodyResults with id favorites_errors_rep_008 [link to favorites_errors_rep_008](./responseBodyResults.md#favorites_errors_rep_008) 

## TC 5.1. Positive Get the favorite airport from Airport Gap account specified by the ID

#### Pre-requisites:
1. Get request with list of all favorited airports details (endpoint: /favorites).

Steps:
1. Add new GET request.
2. Insert baseUrl and endpoint: '/favorites/id' (id from list of the favorit airports).
3. Select an authorization method Bearer token and enter token from collection variables.
4. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 200.  
> 2. Located in file responseBodyResults with id favorites_details_rep_006 [link to favorites_details_rep_006](./responseBodyResults.md#favorites_details_rep_006)

## TC 5.2. Negative Get the favorite airport from Airport Gap account with not existing ID

#### Pre-requisites:
1. Get request with list of all favorited airports details (endpoint: /favorites).

Steps:
1. Add new GET request.
2. Insert baseUrl and endpoint: '/favorites/999999'.
3. Select an authorization method Bearer token and enter token from collection variables.
4. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 404.  
> 2. Located in file responseBodyResults with id get_errors_rep_003 [link to get_errors_rep_003](./responseBodyResults.md#get_errors_rep_003)

## TC 6.1. Positive Update the note of one of favorite airports in your Airport Gap account

#### Pre-requisites:
1. Get request with list of all favorited airports details (endpoint: /favorites).

Steps:
1. Add new PATCH request.
2. Insert baseUrl and endpoint: '/favorites/id' (id from list of the favorit airports).
3. Select an authorization method Bearer token and enter token from collection variables.
4. Update note message in the Params.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 200.  
> 2. Located in file responseBodyResults with id update_favorites_details_rep_009 [link to update_favorites_details_rep_009](./responseBodyResults.md#update_favorites_details_rep_009)

## TC 6.2. Negative Update the note of one of favorite airports in your Airport Gap account with not existing ID

#### Pre-requisites:
1. Get request with list of all favorited airports details (endpoint: /favorites).

Steps:
1. Add new PATCH request.
2. Insert baseUrl and endpoint: '/favorites/999999''.
3. Select an authorization method Bearer token and enter token from collection variables.
4. Update note message in the Params.
5. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 404.  
> 2. Located in file responseBodyResults with id get_errors_rep_003 [link to get_errors_rep_003](./responseBodyResults.md#get_errors_rep_003)

## TC 7.1. Positive Delete one of favorite airports from your Airport Gap account

#### Pre-requisites:
1. Get request with list of all favorited airports details (endpoint: /favorites).

Steps:
1. Add new DELETE request.
2. Insert baseUrl and endpoint: '/favorites/id''.
3. Select an authorization method Bearer token and enter token from collection variables.
4. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 204.  
> 2. Empty response body. 

## TC 7.2. Negative Delete one of favorite airports from your Airport Gap account with not existing ID

#### Pre-requisites:
1. Get request with list of all favorited airports details (endpoint: /favorites).

Steps:
1. Add new DELETE request.
2. Insert baseUrl and endpoint: '/favorites/999999''.
3. Select an authorization method Bearer token and enter token from collection variables.  
4. Click on button Send.

> 🎯 Expected result: 
> 1. Status code 404.  
> 2. Located in file responseBodyResults with id get_errors_rep_003 [link to get_errors_rep_003](./responseBodyResults.md#get_errors_rep_003) 
