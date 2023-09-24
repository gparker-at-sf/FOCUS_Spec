# Usage Type

UsageType is a categorization parameter that defines how a resource or service was consumed during a specified period. The UsageType can influence the price point and also indicate whether purchased commitments are used or unused. This classification offers a nuanced view into the resource or service's consumption patterns and helps in understanding how you're billed, especially when considered alongside attributes like ChargeType and PurchaseType.

The UsageType column MUST be present and MUST NOT be null or empty. This column is of type String and MUST be one of the
allowed values.

See [Appendix: Usage Type](#usagetype-1) for details about allowed values and governance criteria for this dimension.

## Column ID

UsageType

## Display Name

Usage Type

## Description

Indicates whether the record pertains to an on-demand or recurring charge, or relates to the cost or capacity using a committed discount rate or from unutilized commitments.

## Content Constraints

| Constraint      | Value                                    |
| :-------------- | :--------------------------------------- |
| Column required | True                                     |
| Data type       | String                                   |
| Allows nulls    | False                                    |
| Value format    | list-of-values                           |

Allowed values:

| Value      | Description                                                                                                                                                                   |
|:-----------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| On-Demand         | This usage type describes the consumption of resources or services that are billed at the standard on-demand unit price.                                                |
| Interruptible     | The interruptible usage type pertains to resources that are provisioned using spot availability. These resources are billed at a fluctuating spot price, which is typically lower than on-demand prices.                                                                                  |
| Committed         | Committed usage refers to the consumption of resources that benefit from a discounted rate due to long-term commitments, such as reserved instances or savings plans. These resources are billed at this reduced rate. |
| Unused Commitment | This usage type indicates a scenario where a customer has committed to a specific amount or capacity (hourly, daily, etc.) but hasn't fully utilized it. The line item reflects the capacity or monetary value that went unused.                                                                        |

## Introduced (version)

1.0