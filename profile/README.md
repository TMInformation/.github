# Too Much Inventory

An open-source tool for collecting inventory information for On-Prem or Cloud-based environments.


TMI is an open-source tool to discover and collect information from various data sources. The tooling is modular; there is a data source component that should define the parameters for the discovery component to function. 

The data source should be a JSON document that is based on a schema that defines everything that the discovery needs. 

	- What source are we connecting to?
	- How do we connect to the source?
	- What properties are we collecting?
	- How do we define the output?

The discovery tool should consume the data source and return the data defined in the data source document.

It's possible that the JSON document would contain everything required for the discovery tool to do its job. In this scenario, the discovery tool would be a simple binary that executes what is defined in the data source. This places all the logic into the JSON document.

Another possibility would be to have the JSON documents define inputs and outputs. In this scenario, the discovery tool would be more complex, containing all the logic required to collect and generate the data. This allows the discovery tool to be highly focused on the given platform.
