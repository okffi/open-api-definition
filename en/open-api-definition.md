Version: 1.0

Published: 11.10.2014, translated 17.5.2016



# Open API definition

An open Application Programming Interface (API), is an API whose all features are public and which can be used without restricting terms and conditions (for example, it is possible to create an application that utilises the API without explicit approval from the API supplier or mandatory licensing fees).<sup>[1]</sup> This requires that the API description and any related documentation must be openly available and that the API can be freely used to create and test applications. The use of an open API is free of charge. The user does not need to ask permission from the API provider or indicate the intended purpose of usage in advance.

<i>Comment: No fee will be charged for the API documentation and test data. A fee may be charged for access to the actual information content behind the interface even if the API is open.</i>

## Application programming interface (API)

An API determines how the software provides information or services to the applications or other information systems.
<i>Comment: The APIs that are of interest from the perspective of this document are usually Web Service interfaces that are used over the Internet. However, the same principles apply to other interface implementations, as well. The open API definition is independent from the technological implementation methods.</i>

An API can be a simple **data API** through which the data contained by a service can be read to other systems, or it can be a **functional API**, which offers also algorithms or the possibility to change the data in the service via API. If the system has a multiple APIs, it should be specified which of them are open.

<i>Comment: An example of a data API is the interface of the kansalaisaloite.fi online service<sup>[2]</sup>, which provides information on citizens' initiatives. Examples of functional APIs are the Helsinki Region Transport's Journey Planner interface<sup>[3]</sup>, which provides a routing algorithm, and the international Open311 API standard<sup>[4]</sup>, which enables fault reports to be submitted to the compatible city feedback systems.</i>

## Open API

*relationship: holder–user of the interface*

For an API to be called open it must meet the following conditions:

**1) Openly documented:** The API has been specified and the documentation is openly available and accessible over the Internet. The information contained in the system, its structure and the interfaces have been documented at a sufficient level of detail to ensure that the API is as easy as possible to utilise.

<i>Comment: The documentation must be sufficient for independent development without the user having to request additional information from the provider. If the system utilises non-standard data formats, their structure and processing must also be openly and comprehensively documented.</i>

**2) Possible to take into use:** The open API can be taken into use without measures from an administrator or system supplier even outside business hours. Possible registrations are handled automatically.

<i>Comment: This does not need to entail access to the production system and therefore does not preclude access rights management.</i>

**3) Testable:** The API must be testable. At minimum, sample data must be provided for testing purposes. The testability can be implemented in the following ways:
  1. open access to the production system, through which service integration is possible, or

  2. open access to the test system (sandbox), which contains realistic or authentic data, or

  3. the test system can be freely downloaded for installation and any use seen fit

The data available through the open API does not need to be open data<sup>[5]</sup>. The API can be open even if the production system connected to it is entirely isolated from the Internet and can only be accessed by a very limited group of people. If the interface is open but access to the data content is restricted, a test environment that can be accessed openly online must be available.

<i>Comment: The fact that an open API is available for the system does not mean that anyone can access the production system or the information contained by it. For example, a patient information system can involve an open API, but the patient records are not openly accessible. Moreover, an open API can be used to provide information on a particular individual for third parties with individual’s consent  (MyData).</i>

The openness of the APIs enables any party to produce a competing software that implements the same interfaces and is, therefore, compatible with all applications that utilise the API.

## API managed by the client

*relationship: supplier–client*

A client-managed API is an interface that the client is entitled to use and distribute in the way it sees fit. This means that the client can, if it so desires, open the API regardless of the system supplier's stand on the matter. If this is not the case, the API will not be open to external parties and cannot be considered to be an open API.


[1]: http://www.kdk.fi/fi/kokonaisarkkitehtuuri/sanasto
[2]: https://www.kansalaisaloite.fi/api
[3]: http://developer.reittiopas.fi/pages/fi/reittiopas-api
[4]: http://www.open311.org/
[5]: http://opendefinition.org/