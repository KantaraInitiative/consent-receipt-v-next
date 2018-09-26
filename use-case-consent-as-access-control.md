# Use Case: User Consent as Access Control

Author: 
Ryo Kajiwara 

Source: W3C Permissions and User Consent Workshop

Date: 
2018-09-25

# Actors

# Terminology

# Description
We propose describing user consent information in machine-readable standardized format and use it to restrict/filter sensitive information before letting the services use this information. With a standardized description for user consent, app developers can develop privacy-aware applications by being able to parse these documents and filter their data accordingly.  For IoT applications in particular, this aligns well with the Web of Things approach which uses a machine-readable description of potential interactions with IoT devices.

## From a Web of Things perspective: describing data sharing capabilities with Field of Interest

Using the [Web of Things](https://www.w3.org/WoT/) standards, we can describe what information a device can send using a [Thing Description](https://w3c.github.io/wot-thing-description/), which is a JSON-LD document giving the set of interactions available in a thing, along with optional semantic annotation. In addition to this, we can group multiple devices based on what they do using [Field of Interest and iotschema.org](http://iotschema.org/) semantic information. With this information, the user (or an autonomous system acting on their behalf) can figure out what kind of information a device or a group of devices are sending, then decide what information can leave the device and be shared with others.

Standardized user consent data can be used to restrict information from leaving the network by filtering at the gateway, or by telling the device explicitly not to send certain information out of the device.

## Standards of access control / policy description

There are (at least) two relevant standards in the access control domain:

* [XACML](http://xml.coverpages.org/xacml.html)
    * Describes policies in XML format, enables fine-grained attribute-based access control. 
    * Widely used, and many implementations are present, including open-source ones.
    * Drawbacks: they are too heavy-weighted and also based on Mandatory Access Control, where the administrator defines top-down rules for which resources can be accessed by whom.
* Next Generation Access Control(NGAC)
    * https://www.sbir.gov/sbirsearch/detail/1229007
    * https://www.nist.gov/publications/exploring-next-generation-access-control-methodologies
    * https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-178.pdf
    * Uses a dependency graph based model to describe which user or a class of users can access an object or a class of objects.
    * Supports Discretionary Access Control (user defines who can access their objects) efficiently compared to XACML.
    * Not many implementations are present, and lacks a standardized format for describing policies.

From my understanding, there is no standardized/widely-used JSON-based format that describes access control policies and support efficient discretionary access control. There are many services that have discretionary access control and perform well, so I think this combination is not impossible to achieve.

# Outcome
This use case seems to want to use consent data an inputs into access control policy. The consent receipt specification would have to be extended.
