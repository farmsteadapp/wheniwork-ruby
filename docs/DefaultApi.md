# WhenIWork::DefaultApi

All URIs are relative to *https://api.wheniwork.com/2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**payrolls_get**](DefaultApi.md#payrolls_get) | **GET** /payrolls | This method allows you to list payroll periods or find ones within a specified date range.
[**positions_get**](DefaultApi.md#positions_get) | **GET** /positions | This method allows you to get a list of all positions in your account.
[**shifts_get**](DefaultApi.md#shifts_get) | **GET** /shifts | all shifts
[**shifts_shift_id_get**](DefaultApi.md#shifts_shift_id_get) | **GET** /shifts/{shiftId} | Find a shift by id
[**times_get**](DefaultApi.md#times_get) | **GET** /times | get times
[**users_user_id_get**](DefaultApi.md#users_user_id_get) | **GET** /users/{userId} | get user


# **payrolls_get**
> PayrollsResponse payrolls_get(opts)

This method allows you to list payroll periods or find ones within a specified date range.

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

opts = { 
  start: "start_example", # String | 
  _end: DateTime.parse("2013-10-20T19:20:30+01:00") # DateTime | 
}

begin
  #This method allows you to list payroll periods or find ones within a specified date range.
  result = api_instance.payrolls_get(opts)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->payrolls_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start** | **String**|  | [optional] 
 **_end** | **DateTime**|  | [optional] 

### Return type

[**PayrollsResponse**](PayrollsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **positions_get**
> PositionResponse positions_get

This method allows you to get a list of all positions in your account.

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

begin
  #This method allows you to get a list of all positions in your account.
  result = api_instance.positions_get
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->positions_get: #{e}"
end
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PositionResponse**](PositionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **shifts_get**
> ShiftsResponse shifts_get(opts)

all shifts

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

opts = { 
  user_id: 56, # Integer | The ID of the user to get shifts for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3)
  start: "start_example", # String | 
  _end: DateTime.parse("2013-10-20T19:20:30+01:00") # DateTime | 
}

begin
  #all shifts
  result = api_instance.shifts_get(opts)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->shifts_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **Integer**| The ID of the user to get shifts for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3) | [optional] 
 **start** | **String**|  | [optional] 
 **_end** | **DateTime**|  | [optional] 

### Return type

[**ShiftsResponse**](ShiftsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **shifts_shift_id_get**
> Shift shifts_shift_id_get(shift_id)

Find a shift by id

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

shift_id = 789 # Integer | ID of shift to return


begin
  #Find a shift by id
  result = api_instance.shifts_shift_id_get(shift_id)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->shifts_shift_id_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shift_id** | **Integer**| ID of shift to return | 

### Return type

[**Shift**](Shift.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **times_get**
> TimesResponse times_get(opts)

get times

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

opts = { 
  user_id: 56, # Integer | The ID of the user to get times for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3)
  start: "start_example", # String | 
  _end: DateTime.parse("2013-10-20T19:20:30+01:00") # DateTime | 
}

begin
  #get times
  result = api_instance.times_get(opts)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->times_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **Integer**| The ID of the user to get times for. For multiple users, enter a list of user IDs separated by commas (e.g. 1,5,3) | [optional] 
 **start** | **String**|  | [optional] 
 **_end** | **DateTime**|  | [optional] 

### Return type

[**TimesResponse**](TimesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **users_user_id_get**
> UserResponse users_user_id_get(user_id)

get user

### Example
```ruby
# load the gem
require 'wheniwork-ruby'
# setup authorization
WhenIWork.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['W-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['W-Token'] = 'Bearer'
end

api_instance = WhenIWork::DefaultApi.new

user_id = 789 # Integer | ID of shift to return


begin
  #get user
  result = api_instance.users_user_id_get(user_id)
  p result
rescue WhenIWork::ApiError => e
  puts "Exception when calling DefaultApi->users_user_id_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **Integer**| ID of shift to return | 

### Return type

[**UserResponse**](UserResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



