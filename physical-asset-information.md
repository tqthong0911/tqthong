**5.3.1 Physical asset model **

The physical asset model contains information about the physical piece of equipment, usually managed as a physical asset within the enterprise often utilizing a specific serial number. An object in the equipment rnodel defines a role for the equipment, and object in the asset model defines the physical ID and properties of a piece of equipment.

> EXAMPLE Equipment Ds can be represented as TAGs, which define a role such as 7,C18,1 for a temperature controller, while the temperature controller is an asset and has a serial number \(TC\_WED\_O982002022\).
>
> The physlcal asset can be ltd \(e.g because it is broken\) an in that case the TAG will not change, but a new physlcal asset with a unlque sedal number will take the demotion old physical asset. ThereMre t.vo separate ID, are needed, one for the role \(equipment ID\) and one Mr the physlcal asset \(physical asset ID\).

While assets have Level 4 significance, usually because they have an economic value, this part of the standard focuses on the Level 3 significance of the asset. The asset model defines a physical asset as a representation of a physical piece of equipment.

Definitions for hierarchy levels in the physical asset hierarchy are not defined in this Part, however the role-based equipment hierarchy names should be used if they are equivalent.

A representation of physical asset equipment is illustrated in Figure 7.

![](/assets/F-7.png)

**Figure 7— Physical asset model **

The relationship between the physical asset information and the equipment information is shown in Figure 8. There is a temporal relationship between the role of the equipment and the physical asset. The physical asset performing the role may change over time and the equipment asset mapping maintains the association. ![](/assets/F8.png)

**Figure 8— Physical asset and equipment relationship **

> Note This model shown in Figure 8 is consistent with the MIMOSA data models, but with various name differencesdue to their development history

1. A MIMOSA Asset element maps to a Physical Asset object
2. A MIMOSA Asset UtIlization History element maps to an Equipment Asset Mapping object, 
3. A MIMOSA Segment element maps to an EquipmeM object. 
4. A MIMOSA model element maps to a Physical Asset Class object.
5. A MIMOSA Agent element would map to an attribute or property, where needed. 

**5.3.2 Physical asset **

A physical asset represents a physical piece of equipment. Table 16 lists the attributes of a physical asset. A physical asset may be tested by the execution of a physical asset capability test specification.

Physical assets may be made up of other physical assets. For example, a packaging line may be made up of conveyor sections, motors, and sensors.

**Table 16 — Attributes of physical asset**

| Attribute name | Description | Production Examples | Maintenance Examples | Quality Example | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | Defines a unjique identification of a physical asset. | SN5246$9 | SN68928\#1 | SN5247$3 | VIN 55262528 |
| Description | Contains additional information and descriptions of the physical asset. | 2 HP Pump | High PerformancWelder | Auto titration tester | Fork Truck |
| Physical location | Actual physical location of the physical asset | Area 54, Unit 3A | Storage Bay 9982 | Floor 2 lab | Docking Bay 3 |
| Fixed Asset ID | Contains a unique identification for financial tracking as required by laws or regulations. | 2000291 | 2000292 | 2000293 | 2000294 |
| Vendor ID | Contais a vendor's serial number | AT55628 | 667y62 | W78GJ77 | H2228 |

1. The Physical Asset ID should be an enterprise wide identification
2. If an information exchanghe is required to handle assets aross enterpries, then the ID should be a GUID\(Globally Unique ID\)
3. Common local practices may requlre other identifi.tions of physical assets a. require additional correlated identifications represented as properties. 

> NOTE 2 MaMrMis used in maintenance operations may be represented in either the physical asset equlprnent model, in the material model, or in both, when represented in both models Me !Ds used to identify the materMi in both models 15510151 Lot and Physi.1 Asset ID\) should he Me same.

**5.3.3 Physical asset property **

Properties of physical assets shall be listed as physical asset properties. A physical asset shall have zero or more physical asset properties. These specify the current property values of the physical asset for the associated physical asset class property. Physical asset properties may include a unit of measure. Table 17 lists the attributes of a physical asset property. A physical asset property may be tested by the execution of a physical asset capability test specification with results exchanged using a physical asset capability test result.

Physical asset properties may contain nested physical asset properties.

**Table 17— Attributes of physical asset property**

| Attribute Name | Description | Production Examples | Maintnance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of the specific property. | Date of Manyufacture | Assembly Drawing | Tracked Physical Asset | Tracked Physical Asset |
| Description | Additional information about the asset property. | Name plate date of production | Vendor assembly drwaing ID | Indicates that the physical asset must be signed out and tracked | Indicates the state of the physical asset |
| Value | The value, set of values, or range of the property. &lt;br /&gt; The Value\(s\) is assumed to be within the range or set of defined values for the related asset property. | 2008 10 | ACC08-55642 | &lt;Tracked, Not, Tracked&gt; | &lt;Sddigned, Issued, Avaliablle&gt; |
| Value Unit of Measure | The unit of measure of the associated property value, if applicable | Date | String | Boolean | Boolean |

**5.3.4 Physical asset class **

A representation of a grouping of physical assets with similar characteristics for purposes of repair and replacement shall be used as a physical asset class. Any physical asset shall be a member of one physical asset class. Table 18 lists the attributes of a physical asset class. A physical asset class may be tested by the execution of a physical asset capability test specification.

**Table 18 — Attributes of physical asset class **

| Attribute | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Manyfacturer | An identifiation of the manufacture. | Smith Pumps. | Jones Wlders | Franz Testers | Chrysler Fleet Car |
| ID | The manufare's indentification of the specific physical asset class | 2HPWP | HPWLDR 103 | ATT99 | Series K |
| Description | Additional infomation about the physical asset class. | Intrinsically Safe | \(not applicable\) | \(not applicable\) | \(not applicable\) |

**5.3.5  Physical asset class property **

Properties of a physical asset class shall be listed as physical asset class properties. Each may have zero or more recognized properties. Table 19 lists the attributes of a physical asset class property. A physical asset class property may be tested by the execution of a physical asset capability test specification.

Physical asset class properties may contain nested physical asset class properties.

Table 19 — Attributes of physical asset class property

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of the specilfic property | Throughput | Weld rate | Test Speed | Charge Time |
| Description | Additional inforrmation about the property | Pump Throughput | Maximum speed of welder | Average | Hours to recharge |
| Value | The value, set of values, or range of the property. &lt;br /?The value\(s\) is assumed to be within the range or set of defined values for the related asset property | 400 | 5 | 1315 | 5 |
| Value Unit of Measure | The unit of measure of the associated property value, if application | L / Min | cm / Second | Samples / Hour | Hours |

**5.3.6 Physical asset capability test specification **

A representation of a capability test fore physical asset shall be represented as a physical asset capability test specification. A physical asset capability test specification may be associated with a physical asset property. This is typically used where a test is required to ensure that the physical asset has the rated capability and capacity. A physical asset capability test specification may test for one or more physical asset properties. Table 20 lists the attributes of a physical asset capability test specification.

A physical asset capability test specification shall include

a\) an identification of the test;

b\) a version of the test;

c\) a description of the test.

**Table 20 — Attributes of physical asset capability test specification **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of the specific physical asset capability test specification | WPTT82 | WR9 | ATT00029 | CTIME99 |
| Description | Additional information about the test specification | Test of Pump Throughput | Test of Maximum speed of welder | Test of Average test rate | Test of Hours to recharge truck |
| Version | An identification of the version of the capability test specification | 00 | 1 | 3 | 3 |

**5.3.7 Physical asset capability test result**

The results from a qualification test for a specific physical asset shall be represented as a physical capability test result. Table 21 lists the attributes at a physical asset capability test result.

A physical asset capability test result shall include

a\) the date of the test;

b\) the result of the test \(passed-failed or quantitative result\);

c\) the expiration date of the test.

**Table 21 — Attributes of physical asset capability test result **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quallty Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identifiation of the specific physical asset capability test result | CPT-999 | MT-998 | HD-878 | IN-BX-7778 |
| Description | Additional information about the test result. | the number of chrome plated widgets produced per hour | pH meter calibration result test | Hardnees test of unit 878 | Cold box storage temp delta |
| Date | The date and time of the capability test | 1999-10-25 13:30 | 1999-10-25 13:30 | 1999-10-25 13:30 | 1999-10-25 13:30 |
| Result | The result of the capability test | 48 | 7.0001 | &lt;Pass, Fail&gt; | 1.2 |
| Result Unit of Measure | The unit of measure of the associated test result, if applicable | Widgets/Hour | pH | Boolean | ºC |
| Expiration | The date of the expiration of the capability | 2000-10-25 13:30 | 2000-10-25 13:30 | 2000-10-25 13:30 | 2000-10-25 13:30 |

**5.3.8  Equipment asset mapping **

The relationship between a physical asset and an equipment shall be represented as an equipment asset mapping. Table 22 lists the attributes of an equipment asset mapping. The equipment asset mapping records the time period when one equipment object and one physical asset object were associated. 

**Table 22 — Attributes of equipment asset mapping **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of the specific equipment asset mapping | 111 | 112 | 113 | 114 |
| Description | Additional information about the mapping element | \(not applicable\) | Installed under work order 48423. Removed under work order 93823 | \(not applicable\) | \(not applicable\) |
| Start time  | The starting time of the association | 1997-02-10 | 1997-02-10 | 2004-04-23 | 2005-04-30 |
| End Time | The ending time of the association | 2004-12-10 | 2004-12-10 | \(not applicable\) | \(not applicable\) |



