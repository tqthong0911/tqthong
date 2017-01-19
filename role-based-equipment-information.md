
**5.2.1 Role based equipment model **

The role based equipment model shown in Figure 6 contains the information about specific equipment, the classes of equipment, and equipment capability tests.

The formal UML role based equipment model object is used to define the role based equipment hierarchy information that is defined in Part 1 of this standard. The model contains the information that may be used to construct the hierarchical models used in manufacturing scenarios. For purposes of corresponding to the Part 1 models, the defined equipment levels, specified in the Equipment Level attributes, for role based equipment are Enterprise, Site, Area, Work Center, Work Unit, Process Cell, Unit, Production Line, Production Unit, Work Cell, Storage Zone, and Storage Unit.

> NOTE 1 The types of work centers may be extend. when required for application specific role based equipment hlerarchies where the defined types do net apply. When a new type is added 001011 maintain the same relationship witIfin the hlerarchy as the defined work center types \(within an area and containswork units\).

> EXAMPLE 1 Laboratory may be an exMnded equipment level Mat defines a Woik Center Mat includes all equipment In a test lab.

> EXAMPLE 2 A Maintenance Storage CenMr may be an extend. equipment level that d.nes a work Center that Includes all equipment used by maintenance a.vities.

> EXAMPLE 3 A mobile Equlprnent Center may be a work center that includes all mobile equipment whlch may be used at different work centers or areas at different points in time.

![](/assets/F6.png)

**Figure 6— Role based equipment model **

**5.2.2 Equipment class**

Equipment Capability Test Result

An equipment class is a representation of a grouping of equipment with similar characteristics for a definite purpose such as manufacturing operations definition, scheduling, capability and performance. Any piece of equipment may be a member of zero or more equipment classes. Table 10 lists the attributes of equipment class. An equipment class may be tested by the execution of an equipment capability test specification.

NOTE Examples of equipment classes are reactor baffling line, and horizontal Onll press.

**Table 10 — Attributes of equipment class **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique identification of a specific equipment class, within the scope of the information exchanged \(production capability, production shedule, production performance, ......\)<br/>The ID shall be used in other parts of the model when the equipment class needs to be identified, such as the production capability for this requipment class used. | WJ6672892 | Welder | 5662AT | DR-FLT |
| Description | Additional information about the equipment class. | Jigs used to assemble widgets. | Wlder to be signed out | Auto Titration Tester | Deep Reach Fork Truck |
| Equipment Level | An identification of the level in the role based equipment hierarchy. | Production Line | Work Center | Site | Area |

**5.2.3 Equipment class property **

Properties of an equipment class shall be listed as equipment class properties. Each may have zero or more recognized properties. Table 11 lists the attributes of equipment class property. An equipment class property may be tested by the execution of an equipment capability test specification. 

Equipment class properties may contain nested equipment class properties. 

NOTE Examples of equipment class properties fm Me equipment class reactor unit may be linIng material, BTU extraction rate, a. volume. 

**Table 11 — Attributes of equipment class property **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of the specific property. | Template Size | Capactity  | Resolution | Max weight |
| Description | Additional information about the equipment class property. | Range of template sizes for widget machines | Capacity of the weldeer | Minium peak resolution | Maximum carrying weight for the truck |
| Value | The value, set of values, or range of the property. | {10,20,30,40,100,200,300} | {10..400} | {1..10} | {2000 .. 36000} |
| Value Unit of Meeasure | The unit of measure of the associated property value, if applicable | cm | Amperes | ppm | kg |

**5.2.4  Equipment **

A representation of the elements of the equipment hierarchy model shown in Part 1 shall be known as equipment. Equipment may be a listing of sites, areas, production units, production lines, work cells, process cells, units, storage zones or storage units. Table 12 lists the attributes of equipment. Equipment may be tested by the execution of an equipment capability test specification. 

Equipment may be made up of other equipment, as presented in the equipment hierarchy model. EXAMPLE 1 A produollon line may be made up of EXAMPLE 2 A reactor may be rnade up of sensors, valves, an ag.tor, a. level sMtches. 

**Table 12 — Attributes of equipment **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique identification of a specific plece of equipment, within the scope of the information exchanged \(manufacturing operations definition, scheduling, capability and performance\)&lt;br/&gt;The equipment ID shall be used in other parts of the model when the equipment needs to be identified, such as the production capability for a piece of equipment, or a production response identifying the equipment used. | Jig 347 | Widr445 | SN3883AT | VIN28203 |
| Description | Additional information about the equipment. | This is the east side, north building, widget jig | Weilder for north building | Floor 2 lab auto titrator | Shipping dock lift truck |
| Equipment Level | An identification of the level in the role based equipment hierarchy | Production Line | Work center | Site | Area |

**5.2.5 Equipment property **

Properties of equipment shall be listed as equipment properties. An equipment shall have zero or more equipment properties. These specify the current properly values of the equipment for the associated equipment class property. Equipment properties may include a unit of measure. Table 13 lists the attributes of equipment properly. An equipment property may be tested by the execution of an equipment capability test specification with results exchanged in an equipment capability test result. 

Equipment properties may contain nested equipment properties. 

> NOTE: An equipment property may exist elirvutun associatod equipmeM class property, however all parties in an exchange must have a common understanding of the equipment property. 

> EXAMPLE 1 An equipment class property may be volume with a value of \(10000 — 51M001. with a unit of measure of liters, an equipment property rnay be volume with a value of 30.000 and a unit of measure of liters. 

> EXAMPLE 2 Examples of equipment. properties are - other current informallon, such as when calibration is needed; - maintenance status; - the current state of the egulmnent; 

- performance values. 
- other current information, such as when calibration is needed;
- maintenance status;
- the current state of the equipment;
- performance values.

**Table 13— Attributes of equipment property **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of the specific property | Run rate  | Capacity | Resolution | Max weight |
| Description | Additional information about the equipment property. | Widget making average run rate | Capacity of the welder | Minimum peak resolution | Maximum carrying weight for the truck |
| Value | The value, set of values, or range of the property. <br /> The value(s) is assumed to be within the range or set of defined values for the related equipment property.| 59 | {10-200} | 0.05 | 1 |
| Value Unit of Measure | The unit of measure of the associated property value, if applicable | Widgets/Hour | Amperes | % | Tons |

**5.2.6 Equipment capability test specification **

A representation of a capability test shall be presented as an equipment capability test specification. An equipment capability test specification may be associated with an equipment class, equipment class property, equipment or equipment property. This is typically used where a test is required to ensure that the equipment has the necessary capability and capacity. An equipment capability test specification may test for one or more equipment properties. Table 14 lists the attributes of equipment capability test specification. 
An equipment capability test specification shall include 

a) an identification of the test; 

b) eversion of the test; 

c) a description of the test. 

**Table 15 — Attributes of equipment capability test result **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique instance identification that records the results from the execution of a test identified in a capability test specification for a specific plece of equipment. (For example, this may just be a number assigned by the testing authority.) |FQ101/01-10-2000 | WC888 | AT98765 | FS7602 |
| Description | Additional information about the equipment capability test result. | Results from run rate test for JIG 237 for October 1999 | Results from safety check | Results from calibrate | Results from safety check |
| Date | The date and time of the capability test. | 1999-10-25 13:30 | 1999-10-25 13:30 | 1999-10-25 13:30 | 1999-10-25 13:30 |
| Result | The result of thge capability test. | 48 | Fail | Pass | Pass |
| Result Unit of Measure | The date of the expiration of the capability. | Widgets/Hour | <Pass, Fail> | <Pass, Fail> | <Pass, Fail> |
| Expiration | 2000-10-25 13:30 | 2000-10-25 13:30 | 2000-10-25 13:30 | 2000-10-25 13:30 | 2000-10-25 13:30 |

**5.2.8 Containers **
A container for material shall be represented as role based equipment, physical asset, or both of type storage zone or storage unit. 
> EXAMPLE 1 in a refinery; bulk storage tanks would be represented as Storage Units a. as contalners for specific materials. 

> EXAMPLE 2 in an automotive plant; assembly parts Mns would De represented as Storage UMW and as contalners Mr an assembly of pads. 

> EXAMPLE 3 in a pharmaceutical plant; portable tote bins or pallets Mat hold tablets would be represented as Storage UMW for a specltic matedal lot or sublot. 

> EXAMPLE 4 Propedies of containers would be represented as Equipment Class, Equipment, Physlcal Asset Class, or Physical ASSet properties, such as: Readlness, Transpo0ability. Disposable, a. Cleanness. 

The association of material lots and sublots to containers is modeled as properties of the material lot or sublot. 
The association of containers to material lots and sublots is modeled as properties of the container. 

**5.2.9 Tools A tool shall be represented as role based equipment, physical asset, or both.** 

> EXAMPLE 1 in a pharmaceutical plant; a tablet die used to compress a. shape tablets would be represented as a work Unit. The tablet Ole work unit may have properties that Men.. the expected use time a. the actual use time.
 
> EXAMPLE 2 in plastics pads manufacturing; an extruder die would be represent. as a Work U.. The extruder machine could be represented as a Work Cell. 

> EXAMPLE 3 in semiconductor manuM.udno; a rnuiti-platen multi-wafer CLIP (chemical Mechanical Polishing) tool would be represented as a work Cell. 

> EXAMPLE 4 A micrometer used for measurIng sheet metal thickness in a general purpose machine shop may be recorded as equipment but not tracked as a physical asset. 

**5.2.10 Software Software shall be represented as role based equipment, physical asset, or both. **

> NOTE LeVel 3 applications may have responsibliity for keeping the actual software up to date. in the context or this standard, information Mout the software may need to be specified, required, reported or synchronized with Level 0 systems. 

> EXAMPLE 1 when a patch is applied to software the change may need to be known by Level 3 systerns to allow additional testing and Level 6 systems to update secunty settings. 

> EXAMPLE 2 when a physlcal asset is decommissioned and it contains licensed software, Men a Level system may need the InformatIon to order software uninstalls, to order emelt memory cleadng or to know to cancel the maintenance license fee. 

























































































| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID |  |  |  |  |  |
| Description |  |  |  |  |  |
| Name |  |  |  |  |  |
|  |  |  |  |  |  |




```



