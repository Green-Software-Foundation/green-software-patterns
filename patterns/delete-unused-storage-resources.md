# Delete unused storage resources

## Version
1.0

## Submitted By
Sarah Hsu

## Published Date
TBD

## Intent
Delete unused storage resources.

## Tags
Cloud, Storage, Cloud Engineer, Small

## Problem
From an embodied carbon perspective, it's better to delete unused storage resources, so we are efficient with hardware and that the storage layer is optimised for the task. 

## Solution

Delete any unused storage resource

## SCI Impact
`SCI = (E * I) + M per R`

Concerning the SCI equation. Deleting storage volumes will impact one part:
- `M`: By reducing the total number of storage volumes required, we reduce the total embodied carbon.


## Assumptions
If we choose not to delete *ALL* storage resources because they might be needed in the future, then storing them permanently will take up a lot of unnecessary storage resources. A better solution would be removing idle resources, so no hardware is wasted. 

## Pros & Cons
- **PRO**: It may reduce cloud bills, as reducing idle storage resources will cost less. 
- **CON**: We may lose access to data that might be needed in the future