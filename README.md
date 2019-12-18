# ![LOGO](logo.png) The Ubirch web admin API **flow**ground Connector

## Description

A generated **flow**ground connector for the The Ubirch web admin API API (version 0.1.0).

Generated from: /ubirch-web-ui/api/v1<br/>
Generated at: 2019-12-18T08:44:04+00:00

## API Description

Docs for the Ubirch web admin API<br/>

## Authorization

This API does not require authorization.

## Actions

### Simple check.
> Simple check to see if the service is up<br/>

*Tags:* `Check`

### Authenticate
> Authenticate a device against Ubirch device management system. Returns a token if valid, HTTP error code 401 if not<br/>

*Tags:* `Auth`

#### Input Parameters
* `X-Ubirch-Hardware-Id` - _required_ - HardwareId of the device<br/>
* `X-Ubirch-Credential` - _required_ - Password of the device, base64 encoded<br/>

### Get the info of a device
> Get general information about a device.<br/>

*Tags:* `Auth`

#### Input Parameters
* `Authorization` - _required_ - Token of the device. The token can be obtained from the /auth endpoint. Should follow the syntax "bearer TOKEN<br/>

### Add multiple devices.

*Tags:* `Devices`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>

### List all the devices of one user
> For the moment does not support pagination<br/>

*Tags:* `Devices`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `page` - _required_ - Number of the page requested (starts at 0)<br/>
* `size` - _required_ - Number of devices to be contained in a page<br/>

### Search for devices matching a specific attribute
> Search for devices matching a specific attribute: description, hwDeviceId, ...<br/>

*Tags:* `Devices`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `search` - _required_ - String that will be used for the search<br/>

### Number of UPPs that the specified devices created during the specified timeframe

*Tags:* `Devices`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `from` - _required_ - Date in Joda time<br/>
* `to` - _required_ - Date in Joda time<br/>

### Get one device
> Get one device belonging to a user from his hwDeviceId<br/>

*Tags:* `Devices`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `id` - _required_ - hwDeviceId of the device<br/>

### Update a device.
> Update a device. The specified device will see all its attributes replaced by the new provided one.<br/>

*Tags:* `Devices`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `id` - _required_ - hwDeviceId of the device that will be updated<br/>

### Delete a single device
> Delete one device belonging to a user from his hwDeviceId<br/>

*Tags:* `Devices`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `id` - _required_ - hwDeviceId of the device that will be deleted<br/>

### Get all the groups of a user
> see summary<br/>

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>

### Delete a group.
> Delete a group that the user controls.<br/>

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `groupId` - _required_ - Id of the group<br/>

### Add a device into a group
> Add a device into a group. Can only be done if the user is the owner of the device<br/>

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `groupId` - _required_ - Id of the group<br/>
* `hwDeviceIds` - _required_ - HwDeviceIds of the device to be added on the group<br/>

### Get all the devices of a group
> see summary<br/>

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `groupId` - _required_ - Id of the group<br/>

### Check if a group is empty.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `groupId` - _required_ - Id of the group<br/>

### Make a user leave a group.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `groupId` - _required_ - Id of the group<br/>

### Get all the users of a group
> see summary<br/>

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `groupId` - _required_ - Id of the group<br/>

### Create a group and add the user in it
> see summary<br/>

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>
* `groupName` - _required_ - Name of the group<br/>

### Get a user from its Token
> see summary<br/>

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>

### Get a user's basic info
> Get a user's basic info: number of devices and last login<br/>

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Token of the user. ADD "bearer " followed by a space) BEFORE THE TOKEN OTHERWISE IT WON'T WORK<br/>

### Get a user from its username and realm
> see summary<br/>

*Tags:* `Users`

#### Input Parameters
* `username` - _required_ - Username of the user<br/>
* `realmName` - _required_ - Name of the realm where the user is<br/>

## License

**flow**ground :- Telekom iPaaS / the-ubirch-web-admin-api-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
