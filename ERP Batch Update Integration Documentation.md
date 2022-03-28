
### Documenting the integration patterns
![](https://mermaid.ink/svg/pako:eNrFVX9v2jAQ_Speqq6tBE0KqC3ZuglIutJJG1K7dhWpJpMY4hHsyHYoDPHdd05CGn5063-NEPLZdy_v3V3OC8PnATFsYxjxJz_EQqFbx2P7-0gRqRAfohFhRBEfaQeP-RGW0iFDFJAhTiKFhjSK7L1G8_TEPalIJfiYFKbPIy7svWH65IfVJxqo0G7Esw8ltPbDj1avm4O1HMtyTwuwNXN3uMMnmLJnhKZlWU2rQFgzXyTQZUOBwSfxVSJIjlSzBjWMC6Q1czfSLRYjssrL2dn5ebNZhOfmf_PiMQQPDXohVxxkHfY9o-ug1ERgex4zg1SzNCMywv7cpAFhiqq5GRMhOQM71t7m9MQzHo9QhqgfP6L-uISNPCNUKpa2aQ7mybGEHiAxp0wd-3xi2jPblGbHvWkJP6TQBzo3HZ4wn0amO6iKm6TTua9df0uu3Xrjt_X1rttqR-NacNmbXM3Cy9_fx9ZD4zTg963P5OIyFs3rn--xr-iUdEgUXRx0nZTIwbsWEAUumhGkkTKqKGew9WsQYTbO-Gfa5F1dJ6SXGeiuDulAmjyOaS5fmtO6qYVv6i4Q3lh2b8XjdcLdKVT3KhksFqvVcrkpbXXyxspSGvJ1srL_nuBTKuGUshG469KWdnRx85aPkwEohZY-tnRxs-gv2XzaBskPdHz5MAdDZj7YNuDKrk67f7hJxWmjo_U39xHsP78Mfvl5Gys_vJkzv5-udLS2QgFgf3CajoybT6R8XH31zx1arUL-BJE8EeBxeAJfsQGbnzYTtt4iWRhJqwAxEPJyTGkKQBRMmA4WQT5mXgza2NSRcTm_0GUTzAKZIuyuzr8qt4VXgtlN4CNEQHsTwXCEpMKKoAArvKXAaW_UZbfGfJaXCpHdTqshX2S64s6yl94KOhoRsX2JFCE5__xyKLZL-S-uMI8ZFWNCBJgB3MsLzdkzVEgmxDNsWOY3r2d4bAmuSQxiiRtQxYVhD3EkScXAieJaoWEDFbJycigeCTzJvZZ_ASnrs_Y)> **Very much a work in progress**

#### Documenting a Batch Update integration

Documenting a Batch Update integration is the simplest integration to update. The data collected is (all are required):

| Data | Why we need it | Location for the Documentation |
| ----- | ----- | -----|
|Description of the nature of the transactions being submitted|Aids in mapping transactions to the Workday model | D365, attached to the description of the integration|
|Which standard process is used to submit the transactions| Understand the current flow of transactions | D365, attached to the description of the integration |
|Frequency of batch submission|Aids in choosing the most appropriate Workday upload process|D365, attached to the description of the integration |


#### Documenting a Data Fetch integration

For Data Fetch integrations the following needs to be collected:

| Data | Why we need it | Location for the Documentation |
| ----- | ----- | ----- |
|Description of the overall purpose of the integration| Understanding the basic nature of the integration| D365, attached to the description of the integration|
|Frequency of fetch | Understand the impact on the resource | D365, attached to the description of the integration|
|Data consistency requirements| Future delivery methods may vary in their eventual consistency | D365, attached to the description of the integration |
| Method used to fetch the data (API, SQL Query with source database, table, and data elements, etc) | Aids in understanding the current architecture of the integration | D365, attached to the description of the integration |
|For each data element fetched a description of the use of the data elements being fetched (display, calculation, reporting, etc) | This is to aid in determining the matching Workday data elements| Spreadsheet attached to the D365 description of the integration, stored in Teams? Box? GitHub? Russ' laptop?|

#### Documenting a Data Update integration

For Data Update integrations the following data is collected:

| Data | Why we need it | Location for the Documentation |
| ----- | ----- | -----|
|Description of the overall purpose of the integration| Understanding the basic nature of the integration| D365, attached to the description of the integration|
| Method used to update the data (API, SQL Update with source database, table, and data elements, etc) | Aids in understanding the current architecture of the integration | D365, attached to the description of the integration |
| Frequency of update | Understand the volume of updates in order to choose the appropriate future integration pattern | D365, attached to the description of the integration | 
|For each data element updated a description of the purpose of the data element update | This is to aid in determining the matching Workday data elements and update process | Spreadsheet attached to the D365 description of the integration, stored in Teams? Box? GitHub? Doug's laptop?|

#### Documenting a Data Sync integration

Data synchronization integrations tend to be much more complex than the other integration patterns. Most data synchronization integrations utilize a combination of events and data access in order to keep the involved data stores in sync. Thus the documentation required for data sync style integrations is much more involved than for simpler patterns. 



#### Documenting a Initiation of a Business Process integration

TBD


