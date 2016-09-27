# WhenIWork::DefaultApi

All URIs are relative to *https://api.wheniwork.com/2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_positions**](DefaultApi.md#get_positions) | **GET** /positions | 
[**get_shift**](DefaultApi.md#get_shift) | **GET** /shifts/{shift-id} | 
[**get_shifts**](DefaultApi.md#get_shifts) | **GET** /shifts | 
[**get_times**](DefaultApi.md#get_times) | **GET** /times | 
[**get_user**](DefaultApi.md#get_user) | **GET** /users/{user-id} | 
[**get_users**](DefaultApi.md#get_users) | **GET** /users | 


# **get_positions**
> PositionsResponse get_positions(opts)



This method allows you to get a list of all positions in your account.

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

opts = { 
  show_deleted: true # BOOLEAN | Whether to show positions that have been deleted.
}

begin
  result = api_instance.get_positions(opts)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->get_positions: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **show_deleted** | **BOOLEAN**| Whether to show positions that have been deleted. | [optional] 

### Return type

[**PositionsResponse**](PositionsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **get_shift**
> ShiftResponse get_shift(shift_id)



Gets the details of an existing shift.

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

shift_id = 56 # Integer | max records to return


begin
  result = api_instance.get_shift(shift_id)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->get_shift: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shift_id** | **Integer**| max records to return | 

### Return type

[**ShiftResponse**](ShiftResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **get_shifts**
> ShiftsResponse get_shifts(opts)



Get a list of shifts.

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

opts = { 
  user_id: "user_id_example", # String | The ID of the user to get shifts for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3).
  start: DateTime.parse("2013-10-20T19:20:30+01:00"), # DateTime | Start time for the search window. The default is the current date and time
  _end: DateTime.parse("2013-10-20T19:20:30+01:00"), # DateTime | End time for the search window. The default is exactly three days from the start time.
  location_id: "location_id_example", # String | The ID of the location to get shifts for. For multiple locations, enter a list of location IDs separated by commas.
  position_id: "position_id_example", # String | The ID of the position to get shifts for. For multiple position, enter a list of position IDs separated by commas.
  include_open: true, # BOOLEAN | Whether to include OpenShifts in the results.
  include_onlyopen: true, # BOOLEAN | Whether to include OpenShifts in the results.
  unpublished: true # BOOLEAN | Whether unpublished shifts should be included in the results.
}

begin
  result = api_instance.get_shifts(opts)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->get_shifts: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **String**| The ID of the user to get shifts for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3). | [optional] 
 **start** | **DateTime**| Start time for the search window. The default is the current date and time | [optional] 
 **_end** | **DateTime**| End time for the search window. The default is exactly three days from the start time. | [optional] 
 **location_id** | **String**| The ID of the location to get shifts for. For multiple locations, enter a list of location IDs separated by commas. | [optional] 
 **position_id** | **String**| The ID of the position to get shifts for. For multiple position, enter a list of position IDs separated by commas. | [optional] 
 **include_open** | **BOOLEAN**| Whether to include OpenShifts in the results. | [optional] 
 **include_onlyopen** | **BOOLEAN**| Whether to include OpenShifts in the results. | [optional] 
 **unpublished** | **BOOLEAN**| Whether unpublished shifts should be included in the results. | [optional] 

### Return type

[**ShiftsResponse**](ShiftsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **get_times**
> TimesResponse get_times(opts)



Get a list of times

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

opts = { 
  user_id: "user_id_example", # String | The ID of the user to get shifts for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3).
  start: DateTime.parse("2013-10-20T19:20:30+01:00"), # DateTime | Start time for the search window. The default is the current date and time
  _end: DateTime.parse("2013-10-20T19:20:30+01:00") # DateTime | End time for the search window. The default is exactly three days from the start time.
}

begin
  result = api_instance.get_times(opts)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->get_times: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **String**| The ID of the user to get shifts for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3). | [optional] 
 **start** | **DateTime**| Start time for the search window. The default is the current date and time | [optional] 
 **_end** | **DateTime**| End time for the search window. The default is exactly three days from the start time. | [optional] 

### Return type

[**TimesResponse**](TimesResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **get_user**
> UserResponse get_user(user_id)



Get a specific user by their ID.

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

user_id = 56 # Integer | The user identifier number


begin
  result = api_instance.get_user(user_id)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->get_user: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **Integer**| The user identifier number | 

### Return type

[**UserResponse**](UserResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **get_users**
> UsersResponse get_users(opts)



Get a list of users.

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

opts = { 
  ids: "ids_example", # String | The IDs of the users to retrieve, as a comma-separated list (e.g. 9,17,42).
  location_id: "location_id_example", # String | The ID of the location to get users for. For multiple locations, enter a list of location IDs separated by commas.
  show_deleted: true # BOOLEAN | Whether to include deleted users in the results. Defaults to false.
}

begin
  result = api_instance.get_users(opts)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->get_users: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **String**| The IDs of the users to retrieve, as a comma-separated list (e.g. 9,17,42). | [optional] 
 **location_id** | **String**| The ID of the location to get users for. For multiple locations, enter a list of location IDs separated by commas. | [optional] 
 **show_deleted** | **BOOLEAN**| Whether to include deleted users in the results. Defaults to false. | [optional] 

### Return type

[**UsersResponse**](UsersResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



