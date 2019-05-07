# ![LOGO](logo.png) UsageManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the UsageManagementClient API (version 2015-06-01-preview).

Generated from: https://api.apis.guru/v2/specs/azure.com/commerce/2015-06-01-preview/swagger.json<br/>
Generated at: 2019-05-07T17:37:48+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### Enables you to query for the resource/meter metadata and related prices used in a given subscription by Offer ID, Currency, Locale and Region. The metadata associated with the billing meters, including but not limited to service names, types, resources, units of measure, and regions, is subject to change at any time and without notice. If you intend to use this billing data in an automated fashion, please use the billing meter GUID to uniquely identify each billable item. If the billing meter GUID is scheduled to change due to a new billing model, you will be notified in advance of the change.

*Tags:* `RateCard`

#### Input Parameters
* `$filter` - _required_ - The filter to apply on the operation. It ONLY supports the 'eq' and 'and' logical operators at this time. All the 4 query parameters 'OfferDurableId',  'Currency', 'Locale', 'Region' are required to be a part of the $filter.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - It uniquely identifies Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Query aggregated Azure subscription consumption data for a date range.

*Tags:* `UsageAggregates`

#### Input Parameters
* `reportedStartTime` - _required_ - The start of the time range to retrieve data for.
* `reportedEndTime` - _required_ - The end of the time range to retrieve data for.
* `showDetails` - _optional_ - `True` returns usage data in instance-level detail, `false` causes server-side aggregation with fewer details. For example, if you have 3 website instances, by default you will get 3 line items for website consumption. If you specify showDetails = false, the data will be aggregated as a single line item for website consumption within the time period (for the given subscriptionId, meterId, usageStartTime and usageEndTime).
* `aggregationGranularity` - _optional_ - `Daily` (default) returns the data in daily granularity, `Hourly` returns the data in hourly granularity.
    Possible values: Daily, Hourly.
* `continuationToken` - _optional_ - Used when a continuation token string is provided in the response body of the previous call, enabling paging through a large result set. If not present, the data is retrieved from the beginning of the day/hour (based on the granularity) passed in. 
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - It uniquely identifies Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

## License

**flow**ground :- Telekom iPaaS / azure-com-commerce-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
