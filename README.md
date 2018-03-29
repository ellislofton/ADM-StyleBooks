# MAS StyleBooks


This repository contains StyleBooks shipped with MAS and MAS Service (Default StyleBooks) and other StyleBooks that are found useful for the community.

StyleBooks are blueprints that simplify the task of managing complex NetScaler configurations for your applications. A StyleBook is a template that you can use to create and manage NetScaler configurations. You can create a StyleBook for configuring a specific feature of NetScaler, or you can design a StyleBook to create configurations for an enterprise application deployment such as Microsoft Exchange or Google Apps.

StyleBooks fit in well with the principles of Infrastructure-as-code that is practiced by DevOps teams, where configurations are declarative and version-controlled. The configurations are also repeated and are deployed as a whole. StyleBooks offer the following advantages: 

* Declarative: StyleBooks are written in a declarative rather than imperative syntax. Stylebooks allow you to focus on describing the outcome or the "desired state" of the configuration rather than the step-by-step instructions on how to achieve it on a particular NetScaler instance. NetScaler MAS computes the diff between existing state on a NetScaler and the desired state you specified, and makes the necessary edits to the infrastructure. Because StyleBooks use a declarative syntax, written in YAML, components of a StyleBook can be specified in any order, and NetScaler MAS determines the correct order based on their computed dependencies. 
* Atomic: When you use StyleBooks to deploy configurations, the full configuration is deployed or none of it is deployed and this ensures that the infrastructure is always left in a consistent state.
Versioned: A StyleBook has a name, namespace, and a version number that uniquely distinguishes it from any other StyleBook in the system. Any modification to a StyleBook requires an update to its version number (or to its name or namespace) to maintain this unique character. The version update also allows you to maintain multiple versions of the same StyleBook.
* Composable: After a StyleBook is defined, the StyleBook can be used as a unit to build other StyleBooks. You can avoid repeating common patterns of configuration. It also allows you to establish standard building blocks in your organization. Because StyleBooks are versioned, changes to existing StyleBooks results in new StyleBooks, therefore ensuring that dependent StyleBooks are never unintentionally broken.
* App-Centric: StyleBooks can be used to define the NetScaler configuration of a full application. The configuration of the application can be abstracted by using parameters. Therefore, users who create configurations from a StyleBook can interact with a simple interface consisting of filling a few parameters to create what can be a complex NetScaler configuration. Configurations that are created from StyleBooks are not tied to the infrastructure. A single configuration can thus be deployed on one or multiple NetScalers, and can also be moved among instances.
* Auto-Generated UI: NetScaler MAS auto-generates UI forms used to fill in the parameters of the StyleBook when configuration is done using the NetScaler MAS GUI. StyleBook authors do not need to learn a new GUI language or separately create UI pages and forms.
* API-driven: All configuration operations are supported by using the NetScaler MAS GUI or through REST APIs. The APIs can be used in synchronous or asynchronous mode. In addition to the configuration tasks, the StyleBooks APIs also allow you to discover the schema (parameters description) of any StyleBook at runtime.

For a reference on the syntax of StyleBooks and how to write and test new ones, please refer to the Citrix online documentation at: https://docs.citrix.com/en-us/netscaler-mas/12/stylebooks.html

You can also login to MAS, browse the StyleBooks catalog, and see how the different StyleBooks relate to (and depend on) each other, by using the Dependencies Viewer. 

For full documentation on StyleBooks, please refer to NetScaler MAS Online Documentation: https://docs.citrix.com/en-us/netscaler-mas/12/stylebooks.html 
