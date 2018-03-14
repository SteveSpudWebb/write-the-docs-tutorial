# About this task
You can integrate your systems with the GTD platform by calling the APIs. To accomplish your goals, you need to understand the sequence for calling the APIs.
In this example, you will learn how to publish a *Gate in* event as a marine terminal.

The API identifier for *gate in* is: E217 Gate In

<!--this URL will be different based on integration or production and also the version used-->
https://sip-pipeline-integration.mybluemix.net/swagger-ui.html#!/V1_-_Transport_Plan_Events/publishE217UsingPOST_1

The gate in event is also the truck's actual arrival time. It includes all actual gate in events, both on export and import side (which can optionally be indicated by parameter) and for full and empty containers truck moves. The common types of such moves include:
- Actual time of arrival of empty container for export load at stuffing site
- Actual time of arrival of full container at export terminal
- Actual time of arrival of packed container at import inland stripping location
- Actual time of arrival of empty container at depot (terminal or inland location) after stripping

You can supply inputs on the *gate in* API call to associate this event with a container, for example:
- containerTransportRef
- physicalId
- containerTransportId


# Prerequisites
List any prereqs
# Procedure
To publish a *gate in* event as a marine terminal, complete the following steps:
1. Associate this *gate in* with the container using at least one of the following. Note these are listed as optional in the API since only 1 of the 3 is required. They are listed below in order of preference:
   - containerTransportId
   - containerTransportRef
   - physicalId
   <br /><br />
2. Pass the remaining required and optional inputs: <!-- does it make sense to do it this way? -->
   - originatorId (string): The Originator ID
   - originatorName (string): The Originator Name
   - eventSubmissionTime (integer): Time of submission
   - transportationPhase (string): The transportation phase = ['Import', 'Export', 'Transshipment']stringEnum:"Import", "Export", "Transshipment"
   - location (Location)
   - etc
   <br /><br />
3. text


# What to do next


### Another option is to organize with headings like the following:
Similar to https://www.ibm.com/support/knowledgecenter/SSMNED_5.0.0/com.ibm.apic.apionprem.doc/query_3.html

* Name
* Description
* Returns (what the API call returns, just explanation)
* Example call
* Properties (explanation of each field)
* Example result

```
test a code block
put "this is code"
```

Back to [table-of-contents](https://github.com/SteveSpudWebb/write-the-docs-tutorial/blob/master/docs/table-of-contents.md)

