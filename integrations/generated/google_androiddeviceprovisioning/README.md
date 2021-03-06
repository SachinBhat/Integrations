# @datafire/google_androiddeviceprovisioning

Client library for Android Device Provisioning Partner

## Installation and Usage
```bash
npm install --save @datafire/google_androiddeviceprovisioning
```
```js
let google_androiddeviceprovisioning = require('@datafire/google_androiddeviceprovisioning').create();

google_androiddeviceprovisioning.customers.list({}).then(data => {
  console.log(data);
});
```

## Description

Automates Android zero-touch enrollment for device resellers, customers, and EMMs.

## Actions

### customers.list
Lists the user's customer accounts.


```js
google_androiddeviceprovisioning.customers.list({}, context)
```

#### Input
* input `object`
  * pageSize `integer`: The maximum number of customers to show in a page of results.
  * pageToken `string`: A token specifying which result page to return.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [CustomerListCustomersResponse](#customerlistcustomersresponse)

### partners.devices.metadata
Updates reseller metadata associated with the device.


```js
google_androiddeviceprovisioning.partners.devices.metadata({
  "deviceId": "",
  "metadataOwnerId": ""
}, context)
```

#### Input
* input `object`
  * body [UpdateDeviceMetadataRequest](#updatedevicemetadatarequest)
  * deviceId **required** `string`: Required. The ID of the reseller partner.
  * metadataOwnerId **required** `string`: Required. The owner of the newly set metadata. Set this to the partner ID.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [DeviceMetadata](#devicemetadata)

### partners.customers.list
Lists the customers that are enrolled to the reseller identified by the
`partnerId` argument. This list includes customers that the reseller
created and customers that enrolled themselves using the portal.


```js
google_androiddeviceprovisioning.partners.customers.list({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * partnerId **required** `string`: Required. The ID of the reseller partner.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [ListCustomersResponse](#listcustomersresponse)

### partners.devices.claim
Claims a device for a customer and adds it to zero-touch enrollment. If the
device is already claimed by another customer, the call returns an error.


```js
google_androiddeviceprovisioning.partners.devices.claim({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * body [ClaimDeviceRequest](#claimdevicerequest)
  * partnerId **required** `string`: Required. The ID of the reseller partner.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [ClaimDeviceResponse](#claimdeviceresponse)

### partners.devices.claimAsync
Claims a batch of devices for a customer asynchronously. Adds the devices
to zero-touch enrollment. To learn more, read [Long‑running batch
operations](/zero-touch/guides/how-it-works#operations).


```js
google_androiddeviceprovisioning.partners.devices.claimAsync({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * body [ClaimDevicesRequest](#claimdevicesrequest)
  * partnerId **required** `string`: Required. The ID of the reseller partner.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Operation](#operation)

### partners.devices.findByIdentifier
Finds devices by hardware identifiers, such as IMEI.


```js
google_androiddeviceprovisioning.partners.devices.findByIdentifier({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * body [FindDevicesByDeviceIdentifierRequest](#finddevicesbydeviceidentifierrequest)
  * partnerId **required** `string`: Required. The ID of the reseller partner.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [FindDevicesByDeviceIdentifierResponse](#finddevicesbydeviceidentifierresponse)

### partners.devices.findByOwner
Finds devices claimed for customers. The results only contain devices
registered to the reseller that's identified by the `partnerId` argument.
The customer's devices purchased from other resellers don't appear in the
results.


```js
google_androiddeviceprovisioning.partners.devices.findByOwner({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * body [FindDevicesByOwnerRequest](#finddevicesbyownerrequest)
  * partnerId **required** `string`: Required. The ID of the reseller partner.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [FindDevicesByOwnerResponse](#finddevicesbyownerresponse)

### partners.devices.unclaim
Unclaims a device from a customer and removes it from zero-touch
enrollment.


```js
google_androiddeviceprovisioning.partners.devices.unclaim({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * body [UnclaimDeviceRequest](#unclaimdevicerequest)
  * partnerId **required** `string`: Required. The ID of the reseller partner.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Empty](#empty)

### partners.devices.unclaimAsync
Unclaims a batch of devices for a customer asynchronously. Removes the
devices from zero-touch enrollment. To learn more, read [Long‑running batch
operations](/zero-touch/guides/how-it-works#operations).


```js
google_androiddeviceprovisioning.partners.devices.unclaimAsync({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * body [UnclaimDevicesRequest](#unclaimdevicesrequest)
  * partnerId **required** `string`: Required. The reseller partner ID.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Operation](#operation)

### partners.devices.updateMetadataAsync
Updates the reseller metadata attached to a batch of devices. This method
updates devices asynchronously and returns an `Operation` that can be used
to track progress. Read [Long‑running batch
operations](/zero-touch/guides/how-it-works#operations).


```js
google_androiddeviceprovisioning.partners.devices.updateMetadataAsync({
  "partnerId": ""
}, context)
```

#### Input
* input `object`
  * body [UpdateDeviceMetadataInBatchRequest](#updatedevicemetadatainbatchrequest)
  * partnerId **required** `string`: Required. The reseller partner ID.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Operation](#operation)

### customers.configurations.delete
Deletes an unused configuration. The API call fails if the customer has
devices with the configuration applied.


```js
google_androiddeviceprovisioning.customers.configurations.delete({
  "name": ""
}, context)
```

#### Input
* input `object`
  * name **required** `string`: Required. The configuration to delete. An API resource name in the format
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Empty](#empty)

### operations.get
Gets the latest state of a long-running operation.  Clients can use this
method to poll the operation result at intervals as recommended by the API
service.


```js
google_androiddeviceprovisioning.operations.get({
  "name": ""
}, context)
```

#### Input
* input `object`
  * name **required** `string`: The name of the operation resource.
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Operation](#operation)

### customers.configurations.patch
Updates a configuration's field values.


```js
google_androiddeviceprovisioning.customers.configurations.patch({
  "name": ""
}, context)
```

#### Input
* input `object`
  * body [Configuration](#configuration)
  * name **required** `string`: Output only. The API resource name in the format
  * updateMask `string`: Required. The field mask applied to the target `Configuration` before
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Configuration](#configuration)

### customers.configurations.list
Lists a customer's configurations.


```js
google_androiddeviceprovisioning.customers.configurations.list({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * parent **required** `string`: Required. The customer that manages the listed configurations. An API
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [CustomerListConfigurationsResponse](#customerlistconfigurationsresponse)

### customers.configurations.create
Creates a new configuration. Once created, a customer can apply the
configuration to devices.


```js
google_androiddeviceprovisioning.customers.configurations.create({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * body [Configuration](#configuration)
  * parent **required** `string`: Required. The customer that manages the configuration. An API resource name
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Configuration](#configuration)

### partners.customers.create
Creates a customer for zero-touch enrollment. After the method returns
successfully, admin and owner roles can manage devices and EMM configs
by calling API methods or using their zero-touch enrollment portal. The API
doesn't notify the customer that they have access.


```js
google_androiddeviceprovisioning.partners.customers.create({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * body [CreateCustomerRequest](#createcustomerrequest)
  * parent **required** `string`: Required. The parent resource ID in the format `partners/[PARTNER_ID]` that
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Company](#company)

### customers.devices.list
Lists a customer's devices.


```js
google_androiddeviceprovisioning.customers.devices.list({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * pageSize `string`: The maximum number of devices to show in a page of results.
  * pageToken `string`: A token specifying which result page to return.
  * parent **required** `string`: Required. The customer managing the devices. An API resource name in the
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [CustomerListDevicesResponse](#customerlistdevicesresponse)

### customers.devices.applyConfiguration
Applies a Configuration to the device to register the device for zero-touch
enrollment. After applying a configuration to a device, the device
automatically provisions itself on first boot, or next factory reset.


```js
google_androiddeviceprovisioning.customers.devices.applyConfiguration({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * body [CustomerApplyConfigurationRequest](#customerapplyconfigurationrequest)
  * parent **required** `string`: Required. The customer managing the device. An API resource name in the
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Empty](#empty)

### customers.devices.removeConfiguration
Removes a configuration from device.


```js
google_androiddeviceprovisioning.customers.devices.removeConfiguration({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * body [CustomerRemoveConfigurationRequest](#customerremoveconfigurationrequest)
  * parent **required** `string`: Required. The customer managing the device in the format
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Empty](#empty)

### customers.devices.unclaim
Unclaims a device from a customer and removes it from zero-touch
enrollment.

After removing a device, a customer must contact their reseller to register
the device into zero-touch enrollment again.


```js
google_androiddeviceprovisioning.customers.devices.unclaim({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * body [CustomerUnclaimDeviceRequest](#customerunclaimdevicerequest)
  * parent **required** `string`: Required. The customer managing the device. An API resource name in the
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [Empty](#empty)

### customers.dpcs.list
Lists the DPCs (device policy controllers) that support zero-touch
enrollment.


```js
google_androiddeviceprovisioning.customers.dpcs.list({
  "parent": ""
}, context)
```

#### Input
* input `object`
  * parent **required** `string`: Required. The customer that can use the DPCs in configurations. An API
  * $.xgafv `string` (values: 1, 2): V1 error format.
  * access_token `string`: OAuth access token.
  * alt `string` (values: json, media, proto): Data format for response.
  * bearer_token `string`: OAuth bearer token.
  * callback `string`: JSONP
  * fields `string`: Selector specifying which fields to include in a partial response.
  * key `string`: API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
  * oauth_token `string`: OAuth 2.0 token for the current user.
  * pp `boolean`: Pretty-print response.
  * prettyPrint `boolean`: Returns response with indentations and line breaks.
  * quotaUser `string`: Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
  * uploadType `string`: Legacy upload protocol for media (e.g. "media", "multipart").
  * upload_protocol `string`: Upload protocol for media (e.g. "raw", "multipart").

#### Output
* output [CustomerListDpcsResponse](#customerlistdpcsresponse)



## Definitions

### ClaimDeviceRequest
* ClaimDeviceRequest `object`: Request message to claim a device on behalf of a customer.
  * customerId `string`: Required. The ID of the customer for whom the device is being claimed.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)
  * sectionType `string` (values: SECTION_TYPE_UNSPECIFIED, SECTION_TYPE_ZERO_TOUCH): Required. The section type of the device's provisioning record.

### ClaimDeviceResponse
* ClaimDeviceResponse `object`: Response message containing device id of the claim.
  * deviceId `string`: The device ID of the claimed device.
  * deviceName `string`: The resource name of the device in the format

### ClaimDevicesRequest
* ClaimDevicesRequest `object`: Request to claim devices asynchronously in batch. Claiming a device adds the
  * claims `array`: Required. A list of device claims.
    * items [PartnerClaim](#partnerclaim)

### Company
* Company `object`: A customer resource in the zero-touch enrollment API.
  * adminEmails `array`: Input only. Optional. Email address of customer's users in the admin role.
    * items `string`
  * companyId `string`: Output only. The ID of the company. Assigned by the server.
  * companyName `string`: Required. The name of the company. For example _XYZ Corp_. Characters
  * name `string`: Output only. The API resource name of the company in the format
  * ownerEmails `array`: Input only. Email address of customer's users in the owner role. At least
    * items `string`
  * termsStatus `string` (values: TERMS_STATUS_UNSPECIFIED, TERMS_STATUS_NOT_ACCEPTED, TERMS_STATUS_ACCEPTED, TERMS_STATUS_STALE): Output only. Whether any user from the company has accepted the latest

### Configuration
* Configuration `object`: A configuration collects the provisioning options for Android devices. Each
  * companyName `string`: Required. The name of the organization. Zero-touch enrollment shows this
  * configurationId `string`: Output only. The ID of the configuration. Assigned by the server.
  * configurationName `string`: Required. A short name that describes the configuration's purpose. For
  * contactEmail `string`: Required. The email address that device users can contact to get help.
  * contactPhone `string`: Required. The telephone number that device users can call, using another
  * customMessage `string`: A message, containing one or two sentences, to help device users get help
  * dpcExtras `string`: The JSON-formatted EMM provisioning extras that are passed to the DPC.
  * dpcResourcePath `string`: Required. The resource name of the selected DPC (device policy controller)
  * isDefault `boolean`: Required. Whether this is the default configuration that zero-touch
  * name `string`: Output only. The API resource name in the format

### CreateCustomerRequest
* CreateCustomerRequest `object`: Request message to create a customer.
  * customer [Company](#company)

### CustomerApplyConfigurationRequest
* CustomerApplyConfigurationRequest `object`: Request message for customer to assign a configuration to device.
  * configuration `string`: Required. The configuration applied to the device in the format
  * device [DeviceReference](#devicereference)

### CustomerListConfigurationsResponse
* CustomerListConfigurationsResponse `object`: Response message of customer's listing configuration.
  * configurations `array`: The configurations.
    * items [Configuration](#configuration)

### CustomerListCustomersResponse
* CustomerListCustomersResponse `object`: Response message for listing my customers.
  * customers `array`: The customer accounts the calling user is a member of.
    * items [Company](#company)
  * nextPageToken `string`: A token used to access the next page of results. Omitted if no further

### CustomerListDevicesResponse
* CustomerListDevicesResponse `object`: Response message of customer's liting devices.
  * devices `array`: The customer's devices.
    * items [Device](#device)
  * nextPageToken `string`: A token used to access the next page of results. Omitted if no further

### CustomerListDpcsResponse
* CustomerListDpcsResponse `object`: Response message of customer's listing DPCs.
  * dpcs `array`: The list of DPCs available to the customer that support zero-touch
    * items [Dpc](#dpc)

### CustomerRemoveConfigurationRequest
* CustomerRemoveConfigurationRequest `object`: Request message for customer to remove the configuration from device.
  * device [DeviceReference](#devicereference)

### CustomerUnclaimDeviceRequest
* CustomerUnclaimDeviceRequest `object`: Request message for customer to unclaim a device.
  * device [DeviceReference](#devicereference)

### Device
* Device `object`: An Android device registered for zero-touch enrollment.
  * claims `array`: Output only. The provisioning claims for a device. Devices claimed for
    * items [DeviceClaim](#deviceclaim)
  * configuration `string`: Not available to resellers.
  * deviceId `string`: Output only. The ID of the device. Assigned by the server.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)
  * deviceMetadata [DeviceMetadata](#devicemetadata)
  * name `string`: Output only. The API resource name in the format

### DeviceClaim
* DeviceClaim `object`: A record of a device claimed by a reseller for a customer. Devices claimed
  * ownerCompanyId `string`: The ID of the Customer that purchased the device.
  * sectionType `string` (values: SECTION_TYPE_UNSPECIFIED, SECTION_TYPE_ZERO_TOUCH): Output only. The type of claim made on the device.

### DeviceIdentifier
* DeviceIdentifier `object`: Encapsulates hardware and product IDs to identify a manufactured device. To
  * imei `string`: The device’s IMEI number. Validated on input.
  * manufacturer `string`: Required. The device manufacturer’s name. Matches the device's built-in
  * meid `string`: The device’s MEID number.
  * serialNumber `string`: The manufacturer's serial number for the device. This value might not be

### DeviceMetadata
* DeviceMetadata `object`: Metadata entries that can be attached to a `Device`. To learn more, read
  * entries `object`: Metadata entries recorded as key-value pairs.

### DeviceReference
* DeviceReference `object`: A `DeviceReference` is an API abstraction that lets you supply a _device_
  * deviceId `string`: The ID of the device.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)

### DevicesLongRunningOperationMetadata
* DevicesLongRunningOperationMetadata `object`: Tracks the status of a long-running operation to asynchronously update a
  * devicesCount `integer`: The number of metadata updates in the operation. This might be different
  * processingStatus `string` (values: BATCH_PROCESS_STATUS_UNSPECIFIED, BATCH_PROCESS_PENDING, BATCH_PROCESS_IN_PROGRESS, BATCH_PROCESS_PROCESSED): The processing status of the operation.
  * progress `integer`: The processing progress of the operation. Measured as a number from 0 to

### DevicesLongRunningOperationResponse
* DevicesLongRunningOperationResponse `object`: Tracks the status of a long-running operation to claim, unclaim, or attach
  * perDeviceStatus `array`: The processing status for each device in the operation.
    * items [OperationPerDevice](#operationperdevice)
  * successCount `integer`: A summary of how many items in the operation the server processed

### Dpc
* Dpc `object`: An EMM's DPC ([device policy
  * dpcName `string`: Output only. The title of the DPC app in Google Play. For example, _Google
  * name `string`: Output only. The API resource name in the format
  * packageName `string`: Output only. The DPC's Android application ID that looks like a Java

### Empty
* Empty `object`: A generic empty message that you can re-use to avoid defining duplicated

### FindDevicesByDeviceIdentifierRequest
* FindDevicesByDeviceIdentifierRequest `object`: Request to find devices.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)
  * limit `string`: Required. The maximum number of devices to show in a page of results. Must
  * pageToken `string`: A token specifying which result page to return.

### FindDevicesByDeviceIdentifierResponse
* FindDevicesByDeviceIdentifierResponse `object`: Response containing found devices.
  * devices `array`: Found devices.
    * items [Device](#device)
  * nextPageToken `string`: A token used to access the next page of results. Omitted if no further

### FindDevicesByOwnerRequest
* FindDevicesByOwnerRequest `object`: Request to find devices by customers.
  * customerId `array`: Required. The list of customer IDs to search for.
    * items `string`
  * limit `string`: Required. The maximum number of devices to show in a page of results. Must
  * pageToken `string`: A token specifying which result page to return.
  * sectionType `string` (values: SECTION_TYPE_UNSPECIFIED, SECTION_TYPE_ZERO_TOUCH): Required. The section type of the device's provisioning record.

### FindDevicesByOwnerResponse
* FindDevicesByOwnerResponse `object`: Response containing found devices.
  * devices `array`: The customer's devices.
    * items [Device](#device)
  * nextPageToken `string`: A token used to access the next page of results.

### ListCustomersResponse
* ListCustomersResponse `object`: Response message of all customers related to this partner.
  * customers `array`: List of customers related to this reseller partner.
    * items [Company](#company)

### Operation
* Operation `object`: This resource represents a long-running operation that is the result of a
  * done `boolean`: If the value is `false`, it means the operation is still in progress.
  * error [Status](#status)
  * metadata `object`: This field will contain a `DevicesLongRunningOperationMetadata` object if the operation is created by `claimAsync`, `unclaimAsync`, or `updateMetadataAsync`.
  * name `string`: The server-assigned name, which is only unique within the same service that
  * response `object`: This field will contain a `DevicesLongRunningOperationResponse` object if the operation is created by `claimAsync`, `unclaimAsync`, or `updateMetadataAsync`.

### OperationPerDevice
* OperationPerDevice `object`: A task for each device in the operation. Corresponds to each device
  * claim [PartnerClaim](#partnerclaim)
  * result [PerDeviceStatusInBatch](#perdevicestatusinbatch)
  * unclaim [PartnerUnclaim](#partnerunclaim)
  * updateMetadata [UpdateMetadataArguments](#updatemetadataarguments)

### PartnerClaim
* PartnerClaim `object`: Identifies one claim request.
  * customerId `string`: Required. The ID of the customer for whom the device is being claimed.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)
  * deviceMetadata [DeviceMetadata](#devicemetadata)
  * sectionType `string` (values: SECTION_TYPE_UNSPECIFIED, SECTION_TYPE_ZERO_TOUCH): Required. The section type of the device's provisioning record.

### PartnerUnclaim
* PartnerUnclaim `object`: Identifies one unclaim request.
  * deviceId `string`: Device ID of the device.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)
  * sectionType `string` (values: SECTION_TYPE_UNSPECIFIED, SECTION_TYPE_ZERO_TOUCH): Required. The section type of the device's provisioning record.

### PerDeviceStatusInBatch
* PerDeviceStatusInBatch `object`: Captures the processing status for each device in the operation.
  * deviceId `string`: If processing succeeds, the device ID of the device.
  * errorIdentifier `string`: If processing fails, the error type.
  * errorMessage `string`: If processing fails, a developer message explaining what went wrong.
  * status `string` (values: SINGLE_DEVICE_STATUS_UNSPECIFIED, SINGLE_DEVICE_STATUS_UNKNOWN_ERROR, SINGLE_DEVICE_STATUS_OTHER_ERROR, SINGLE_DEVICE_STATUS_SUCCESS, SINGLE_DEVICE_STATUS_PERMISSION_DENIED, SINGLE_DEVICE_STATUS_INVALID_DEVICE_IDENTIFIER, SINGLE_DEVICE_STATUS_INVALID_SECTION_TYPE, SINGLE_DEVICE_STATUS_SECTION_NOT_YOURS): The result status of the device after processing.

### Status
* Status `object`: The `Status` type defines a logical error model that is suitable for different
  * code `integer`: The status code, which should be an enum value of google.rpc.Code.
  * details `array`: A list of messages that carry the error details.  There is a common set of
    * items `object`
  * message `string`: A developer-facing error message, which should be in English. Any

### UnclaimDeviceRequest
* UnclaimDeviceRequest `object`: Request message to unclaim a device.
  * deviceId `string`: The device ID returned by `ClaimDevice`.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)
  * sectionType `string` (values: SECTION_TYPE_UNSPECIFIED, SECTION_TYPE_ZERO_TOUCH): Required. The section type of the device's provisioning record.

### UnclaimDevicesRequest
* UnclaimDevicesRequest `object`: Request to unclaim devices asynchronously in batch.
  * unclaims `array`: Required. The list of devices to unclaim.
    * items [PartnerUnclaim](#partnerunclaim)

### UpdateDeviceMetadataInBatchRequest
* UpdateDeviceMetadataInBatchRequest `object`: Request to update device metadata in batch.
  * updates `array`: Required. The list of metadata updates.
    * items [UpdateMetadataArguments](#updatemetadataarguments)

### UpdateDeviceMetadataRequest
* UpdateDeviceMetadataRequest `object`: Request to set metadata for a device.
  * deviceMetadata [DeviceMetadata](#devicemetadata)

### UpdateMetadataArguments
* UpdateMetadataArguments `object`: Identifies metdata updates to one device.
  * deviceId `string`: Device ID of the device.
  * deviceIdentifier [DeviceIdentifier](#deviceidentifier)
  * deviceMetadata [DeviceMetadata](#devicemetadata)


