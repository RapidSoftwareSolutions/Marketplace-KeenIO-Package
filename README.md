[![](https://scdn.rapidapi.com/RapidAPI_banner.png)](https://rapidapi.com/package/KeenIO/functions?utm_source=RapidAPIGitHub_KeenIOFunctions&utm_medium=button&utm_content=RapidAPI_GitHub)


# KeenIO Package
APIs for capturing, analyzing, and embedding event data in everything you build.
* Domain: [keen.io](https://keen.io)
* Credentials: masterKey, writeKey, readKey, organizationKey, accessKey

## How to get credentials: 
1. Sign in [keen.io](https://keen.io).
2. Create new project.
3. Navigate to project->access.

## Custom datatypes:
  |Datatype|Description|Example
  |--------|-----------|----------
  |Datepicker|String which includes date and time|```2016-05-28 00:00:00```
  |Map|String which includes latitude and longitude coma separated|```50.37, 26.56```
  |List|Simple array|```["123", "sample"]```
  |Select|String with predefined values|```sample```
  |Array|Array of objects|```[{"Second name":"123","Age":"12","Photo":"sdf","Draft":"sdfsdf"},{"name":"adi","Second name":"bla","Age":"4","Photo":"asfserwe","Draft":"sdfsdf"}] ```
 
## KeenIO.createEvent
Records a single event to a given event collection.

| Field         | Type       | Description
|---------------|------------|----------
| writeKey      | Credentials| Your write key
| projectId     | String     | Project identifier.
| collectionName| String     | Collection name.
| data          | JSON       | Event body.

## KeenIO.createMultipleEvents
Record multiple events across one or more event collections.

| Field    | Type       | Description
|----------|------------|----------
| writeKey | Credentials| Your write key
| projectId| String     | Project identifier.
| data     | JSON       | Event body.

## KeenIO.getSingleEventCollection
Return schema information for a single event collection.

| Field         | Type       | Description
|---------------|------------|----------
| readKey       | Credentials| Your read key
| projectId     | String     | Project identifier.
| collectionName| String     | Collection name.

## KeenIO.getAllCollections
Return schema information for all the event collections in a given project.

| Field    | Type       | Description
|----------|------------|----------
| readKey  | Credentials| Your read key
| projectId| String     | Project identifier.

## KeenIO.getEventsCount
Return the number of events in the collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred. Example: ```this_7_days```

## KeenIO.getUniqueEventsCount
Return the number of events with unique values, for a target property in a collection matching given criteria. A common use for this is to count the number of unique users who performed an event.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.

## KeenIO.getMinimumValue
Return the minimum numeric value for a target property, among all events in a collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.

## KeenIO.getMaximunValue
Return the maximum numeric value for a target property, among all events in a collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.

## KeenIO.calculatePropertyValues
Calculate the sum of all numeric values for a target property, among all events in a collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.

## KeenIO.calculateAveragePropertyValues
Calculate the average value for a target property, among all events in a collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.

## KeenIO.calculateMedianPropertyValues
Calculate the median value for a target property, among all events in a collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.

## KeenIO.calculatePercentileValue
Calculate a specified percentile value for a target property, among all events in a collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.
| percentile     | String     | Specifies the percentile to calculate, supporting 0-100 with two decimal places of precision. Example: 99.99.

## KeenIO.getUniqueValues
Return a list of unique property values for a target property, among all events in a collection matching given criteria.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| targetProperty | String     | Specifies the name of the property to analyze.
| timeframe      | String     | Limits analysis to a specific period of time when the events occurred.

## KeenIO.createSavedQuery
Creating a Saved Query.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| query    | JSON       | Parameters for the query you want to save and have us run on an interval.
| queryName| String     | Query name.

## KeenIO.getSavedQueryResult
Getting Saved Query Results.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| queryName| String     | Query name.

## KeenIO.updateSavedQuery
To change the definition of the query, you must provide a complete new definition for the query in the “query” field in the body.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| query    | JSON       | Parameters for the query you want to save and have us run on an interval.
| queryName| String     | Change the name of the query.

## KeenIO.getAllSavedQueries
Getting All Saved Query Definitions.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.

## KeenIO.getSingleSavedQuery
Getting a Saved Query Definition.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| queryName| String     | Change the name of the query.

## KeenIO.deleteSavedQuery
Delete a Saved Query.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| queryName| String     | Change the name of the query.

## KeenIO.createCachedQuery
By turning on caching, you can tell Keen to automatically refresh your saved queries so you can get immediate results. We will calculate the results of your query on a set interval, and have them available for you immediately when you ask for the Saved Query result.

| Field      | Type       | Description
|------------|------------|----------
| masterKey  | Credentials| Your master key
| projectId  | String     | Project identifier.
| queryName  | String     | Change the name of the query.
| refreshRate| String     | The refresh rate value is in seconds, and must be more than 1 hour (3,600 seconds) and less than 24 hours (86,400 seconds).

## KeenIO.createCachedDataset
Create a Cached Dataset.

| Field      | Type       | Description
|------------|------------|----------
| masterKey  | Credentials| Your master key
| projectId  | String     | Project identifier.
| datasetName| String     | Dataset identifier.
| query      | JSON       | The query definition you want Keen to optimize for your application. 
| indexBy    | String     | The event property name of string values you will to retrieve results by; eg “product.id” stored as “1f2o3o4”, “5b6a7r8”. Currently supports one index_by property name. Cannot duplicate property query’s group_by.
| displayName| String     | The human-readable string name for your Cached Dataset

## KeenIO.getSingleDataset
Getting a Dataset Definition.

| Field      | Type       | Description
|------------|------------|----------
| readKey    | Credentials| Your read key
| projectId  | String     | Project identifier.
| datasetName| String     | Dataset identifier.

## KeenIO.getCachedDatasetResult
Retrieving results from a Cached Dataset.

| Field      | Type       | Description
|------------|------------|----------
| readKey    | Credentials| Your read key
| projectId  | String     | Project identifier.
| datasetName| String     | Dataset identifier.
| indexBy    | String     | The string property value you want to retrieve results by.
| timeframe  | String     | Limits retrieval of results to a specific portion of the Cached Dataset.

## KeenIO.getProjectDatasets
Get list of Cached Dataset definitions for a project

| Field    | Type       | Description
|----------|------------|----------
| readKey  | Credentials| Your read key
| projectId| String     | Project identifier.
| limit    | Number     | How many Cached Dataset definitions to return at a time (1-100). Defaults to 10.
| afterName| String     | A cursor for use in pagination. after_name is the Cached Dataset name that defines your place in the list. For instance, if you make a list request and receive 100 Cached Dataset definitions, ending with dataset_foo you can use dataset_foo as your after_name to retrieve the next page of definitions. Lists also return with helper “next_page_url” that uses after_name, so your subsequent call can fetch the next page of the list easily.

## KeenIO.deleteCachedDataset
Delete a Cached Dataset.

| Field      | Type       | Description
|------------|------------|----------
| masterKey  | Credentials| Your master key
| projectId  | String     | Project identifier.
| datasetName| String     | Dataset identifier.

## KeenIO.getProjectQueries
Return a list of available query resources with a GET request.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.

## KeenIO.createExtractionRequest
Creates an extraction request for full-form event data with all property values.

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| timeframe      | String     | Refines the scope of events to be included in the analysis based on when the event occurred.
| filters        | String     | Refines the scope of events to be included in the analysis based on event property values.
| timezone       | String     | Assigns a timezone offset to relative timeframes.
| email          | String     | If an email address is specified, an email will be sent to it when your extraction is ready for download. If email is not specified, your extraction will be processed synchronously and your data will be returned as JSON.
| latest         | Number     | An integer containing the number of most recent events to extract.

## KeenIO.extractToCSV
Extract to CSV file

| Field          | Type       | Description
|----------------|------------|----------
| readKey        | Credentials| Your read key
| projectId      | String     | Project identifier.
| eventCollection| String     | Specifies the name of the event collection to analyze.
| timeframe      | String     | Refines the scope of events to be included in the analysis based on when the event occurred.
| email          | String     | Email address.

## KeenIO.getSingleProject
Returns information about a project.

| Field          | Type       | Description
|----------------|------------|----------
| organizationKey| Credentials| Your organization key
| organizationId | String     | Organization identifier.
| projectId      | String     | Project identifier.

## KeenIO.getAllProjects
Returns information about all projects for the given organization.

| Field          | Type       | Description
|----------------|------------|----------
| organizationKey| Credentials| Your organization key
| organizationId | String     | Organization identifier.

## KeenIO.createProject
Create a new project in the organization.

| Field          | Type       | Description
|----------------|------------|----------
| organizationKey| Credentials| Your organization key
| organizationId | String     | Organization identifier.
| name           | String     | Specifies the name of the project to be created.
| users          | Array      | Specifies users for the project. If any users supplied do not exist, the request will fail. You will receive an error indicating which users are invalid.

## KeenIO.updateProject
Update an existing project in the organization.

| Field          | Type       | Description
|----------------|------------|----------
| organizationKey| Credentials| Your organization key
| organizationId | String     | Organization identifier.
| projectId      | String     | Project identifier.
| name           | String     | Specifies the name of the project to be created.
| users          | Array      | Specifies users for the project. If any users supplied do not exist, the request will fail. You will receive an error indicating which users are invalid.

## KeenIO.createAccessKey
Create a new API Key for the project.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| name     | String     | A human readable name for the API Key. Limited to 256 characters.
| isActive | Select     | A boolean that indicates if the key is currently active or revoked.
| permitted| List       | A list of high level actions this key can perform. Possible options: “writes”, “queries”, “saved_queries”, “cached_queries”, “datasets”, “schema”
| options  | JSON       | An object containing more details about the key’s permitted and restricted functionality.

## KeenIO.getAllAccessKeys
Retrieves a list of Access Keys.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.

## KeenIO.getSingleAccessKey
Retrieves an Access Key definition.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| customKey| String     | Key identifier.

## KeenIO.revokeAccessKey
Revoking an Access Key.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| customKey| String     | Key identifier.

## KeenIO.unrevokeAccessKey
Unrevokes an Access Key.

| Field    | Type       | Description
|----------|------------|----------
| masterKey| Credentials| Your master key
| projectId| String     | Project identifier.
| customKey| String     | Key identifier.

## KeenIO.deleteCollection
Delete a single event collection.

| Field         | Type       | Description
|---------------|------------|----------
| masterKey     | Credentials| Your master key
| projectId     | String     | Project identifier.
| collectionName| String     | Collection name.

## KeenIO.deleteEvents
Deletes events meeting criteria of supplied filters, timeframe and timezone parameters

| Field         | Type       | Description
|---------------|------------|----------
| masterKey     | Credentials| Your master key
| projectId     | String     | Project identifier.
| collectionName| String     | Collection name.
| filters       | String     | Optional filters to use when selecting events for deletion.
| timeframe     | String     | Optional timeframes to use when selecting events for deletion.
| timezone      | String     | Optional timezone to use when specifying a timeframe.

## KeenIO.deleteProperty
Delete a Property.

| Field         | Type       | Description
|---------------|------------|----------
| masterKey     | Credentials| Your master key
| projectId     | String     | Project identifier.
| collectionName| String     | Collection name.
| propertyName  | String     | Property name.

