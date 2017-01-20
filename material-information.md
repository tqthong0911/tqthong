**5.4.1 Material model **

The material model shown in Figure 9 defines the actual materials, material definitions, and information about classes of material definitions. Material information includes the inventory of raw, finished, intermediate materials, and consumables. The information about planned or actual material is contained in the material lot and material sublet information. Material classes are defined to organize materials.

> NOTE Thls corresponds to a resource model Mr material, as defined in ISO 10303.

![](/assets/F-9.png)

**Figure 9 — Material model **

**5.4.2 Material class**

A material class is a representation of groupings of material definitions for a definite purpose such as manufacturing operations definition, scheduling, capability and performance. Table 23 lists the attributes of material class. A material class may be tested by the execution of a material test specification.

> NOTE An example of a material class may be sweetener, with members of fmctase, corn syrup, a. sugar cane syrup, Another example of a material class may be wafer, with members of clly waMr, recycled water, and spring water,

A material definition shall belong to zero or more material classes.

**Table 23 — Attributes of material class **

| Attribute Name | Description | Production Exapmles | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique identification of a specific material class, within the scope of the information exchanged \(production capability, production schedule, production performance, ...\)&lt;br /&gt;The ID shall be used in other parts of the model when the material class needs to be identified, such as the production capability for this material class, or a production response identifying the material class used. | Polymer sheet stock 1001A | 200 cP Oil \(SAE 90\) | RH5510 | 200 mil Wrap |
| Description | Additional information about the material class. | Solid polymer resin | Very High Viscosity Lubricating Oil | Oxidizing Agent | Wrap used to wrap pallets |
| Assembly Type | Optional: Defines the type of the assembly. The defined types are: &lt;br /&gt;Physical - The compnents of the assembly are physically connected or in the same area.&lt;br /&gt;Logical - The components of the assembly are not necessarily physically connected or in the same area. | Physical | Physical | Logical | Physical |
| Assembly Relationship | Optional: Defines the type of the relationships. The defined types are: &lt;br /&gt; Permanet - An assembly that is not intended to be split during the production process.&lt;br /&gt;Transient - A temporary assembly using during production, such as a pallet of different materials or a batch kit. | Permanent | Transient | Permanet | Transient |

A material class may be defined as containing an assembly of material classes and as part of an assembly of material classes:

1. A material class rnay define an assembly of zero or more material classes. 
2. A material class rnay be an assembly element 00 0000 or more material classes. 
3. An assembly may be defined as a permanent or transient assembly of material classes. 
4. An assembly may be defined as physical or a logical assembly of material classes. 

**5.4.3  Material class property **

Properties of a material class shall be presented as material class properties. A material class shall be further characterized through zero or more material class properties. Table 24 lists the attributes of material class property. A material class properly may be tested by the execution of a material test specification.

Material class properties may contain nested material class properties.

> NOTE Examples of material class propertles include density, pH factor, and material strength.

The material class properties often list the nominal, or standard, values for the material. A material property does not have to match a material class property.

**Table 24 — Attributes of material class property **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of a specific material class property. | Polyethylene sheet thickness | Oil Viscosity | pH | Weight |
| Description | Additional infomation about the material class oproperty | Sheet Thickness | Coefficient of viscosity | Acidity | Weight to be added to shipping label |
| Value | The value, set of values, or range of the property | {5,10,25} | \(not applicable\) | {0..7} | \(not applicable\) |
| Value Unit of Measure | The unit of measure of the associated prperty value, if applicable | mm | Pa-s | pH | g / $'m^2'$ |

**5.4.4 Material definition **

A representation of goods with similar name charaderistics for the purpose of manufacturing operations de nition, scheduling, capability and performance shall be shown as a material definition. Tab a 25 lists the attributes of material definition. A material definition may be tested by the execution of a material test specification.

> NOTE Ex moles M these may be city water, hydrochionc acid and grade B aluminum.

Any material lot shall be associated with one material definition.

**Table 25 — Attributes of material definition **

| ID | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
|  | A unique identification of a specific material definition, within the scope of the information exchanged \(production capability, production schedule, production performance,...\)&lt;br /&gt;The ID shall be used in other parts of the model when the material definition needs to be indentified, such as the production capability for this material definition, or a production response identifying the material definition used. | Sheet stock 1443a | DO200cpO | OA9929 | PW882929 |
| Description | Additional information about the material definition | General purpose sheet stock | 200 cP Oil from Dino Oil | Oxidizing Agent from  RustitAil | General purpose 20 mil wrap |
| Assembly Type | Optional: Defines the type assembly. The defined types are:&lt;br /&gt;Physical - The components of the assembly are physically connected or in the same area | Physical | Physical | Logical | Physical |
| Assembly Relationship | Optional: Defines the type of the relationships. The defined types are: &lt;br /&gt;Permanent — An assembly that is not intended to spilt during the production process.&lt;br /&gt;Transient — A temporary assembly using during production, such as a pallet of different materials pr a batch kit. | Permanent | Transient | Permanent | Transient |

A material def nition may be defined as containing en assembly of material definitions and as part of an assembly of material definitions:

1. A material definition rnay define an assembly of zero or more material definitions. 
2. A mate ial definition may be an assembly element of zero or more material definitions. 
3. An as em Sly may be defined as a permanent or transient assembly of material definitions. 
4. An assembly may be defined as physical or a logical assembly of material definitions. 

**5.4.5  Material definition property **

Properties of a material definition shall be defined as material definition properties. A material definition shall be further characterized through zero or more material definition properties.

Table 26 lists the attributes of material definition properly. A material definition property may be tested by the execution of a material test specification.

Material definition properties may contain nested material definition properties.

> NOTE Examples of material definition property Include density, pH factor, or material strength, Properties may present the nominal or standard values for the material.

**Table 26 — Attributes of material definition property**

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An idenfication of the specific material definffion property | 1443a5mm | Oil Viscosity | pH | Weight |
| Description | Additional InformatIon about the material definition property. | 5 millimeter sheet | Coefficient of viscosdy | Acidity | WeIght to be added to shipping label |
| Value | The vaffie, set of values, or range of the property. | {4.85 .. 5.11} | {250 x 10^-3 .. 255 x 10^-3} | {3.99 .. 4.01} | 20 .. 21 |
| Value Unit of Measure | The unit of measure of the associated property value, if applicable | mm | Pa-s | pH | g/m^2 |

**5.4.6 Material lot **

A representation of a uniquely identified specific amount of material, either countable or weighable shall be named as a material lot A material lot describes the planned or actual total quantity or amount of material available, its current state, and its specific property values. Table 27 lists the alt ibutes of material lot. A material lot may be tested by the execution of a material test specification.

A material lot shall include a\) a unique identification of the lot; b\) the amount of material \(count, volume, weight\); c\) the unit of measure of the material for example, pads, liters, kg\); d\) a storage location for the material; e\) any status of the lot.

A material lot may be made up of material sublets. Material lots and material sublets may be used for traceability when they contain unique identifications.

**Table 27 - Attributes of material lot**

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique identification of a specific material definition, within the scope of the information exchanged \(production capability, production schedule, production performance,...\)&lt;br /&gt;The ID shall be used in other parts of the model when the material definition needs to be indentified, such as the production capability for this material definition, or a production response identifying the material definition used. | L66729-99 | L8828-81 | L53920-02 | L8626-33 |
| Description | Additional information about the material lot | PlastiFab 10/31 shipment | Oil | Reagent | Wrapping material |
| Assembly Type | Optional: Defines the type assembly. The defined types are:&lt;br /&gt;Physical - The components of the assembly are physically connected or in the same area | Physical | Physical | Logical | Physical |
| Assembly Relationship | Optional: Defines the type of the relationships. The defined types are: &lt;br /&gt;Permanent — An assembly that is not intended to spilt during the production process.&lt;br /&gt;Transient — A temporary assembly using during production, such as a pallet of different materials pr a batch kit.&lt;br /&gt;Note 2 If material lost \(or sublots\) are merged or absorbed \(e.g. blended\), then this is a new material lot, as defined in Part 1 of this standard, not an assembly | Permanent | Transient | Permanent | Transient |
| Status | Status of the material lot. For example, released, approved, blocked, in process, in quality check. | Work center 1 | Maintenance Shed 4S | Work Bench 10, Top Shelf | Warehouse 1 |
| Quantity | The quantity of the material lot. | 1200 | 20 | 1 | 41 |
| Quantity Unit of Measure | The unit of measure of the associated quantity, if applicable | sheets | Cans | liter | rolls |

> NOTE 2 if non-lot .ntrolled Items must be maintain. In multiple locations then the inbrmallon may be represented In the Material Sublot model through the use of unique sublot lOs Mr ea. different location a. Materlai Definition.

A material lot or a material sublet may be defined as containing an assembly of material lots or material sublets and as part of an assembly of material lots or material sublets:

1. A material lot or a material sublet may define an assembly of zero or more material lots or a material sublets. 
2. A material lot or a material sublet may be an assembly element of zero or more material lots or a material sublets. 
3. An assembly may be defined as a permanent or transient assembly of material lots or sublets. 
4. > EXAMPLE 1 A translent assembly could be a temporary collection of maMrial maintalned as a batch kit on a pailM, the bat. klt Is Identified with a unique identification and may contain specific properties, such as a pallet identification, location. and related bat. ID.
   >
   > EXAMPLE 2 A permanent assembly of material may be an automobile. The automobile has a unlque vehlcie Identification number \(VIN\) and other properties. The automobile may contain an assembly of an englne, transmission, chassis, and wheels, each with their own unlque identificallon a. properties.
5. An assembly may be defined as physical or a logical assembly of material or sublets. Assemblies of materials do not imply a manufacturing status.

> EXAMPLE 3 A finIshed traMor is a physlcal assemMy of matedais.
>
> EXAMPLE 4 An unassembled collection of tractor components that are separately shipped is a logical assembly of materials.

**5.4.7 Material lot property **

Each material can have unique values for zero or more material lot properties, such as a specific pH value for the specific lot of material, or a specific density tor the lot of material. A material lot property may be tested by the execution of a material test specification with results exchanged in a QA test specification result.

Material lot properties may contain nested material lot properties.

A material lot property is associated with either a material lot or a material sublet. When associated with a material lot it specifies a properly value for all sublets, when associated with a material sublet it specifies a property value fora single sublet.

**Table 28 lists the attributes of material lot property. **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identlfIcation of the speciflc material iot property | Average sheet thickness | Oil Viscosity | pH | Weight |
| Description | Additional information about the material iot property | Measured thickness | Coefficient of viscosity | Acidity | weight to be added to shipping label |
| Value | The value, set of values, or range of the property. | 5.002 | 230 x 10^-3 | 4.01 | 20.3 |
| Value Unit of Measure | The unit of measure of the associated property value, if applicable. | mm | Pa-s | pH | g / m^2 |

**5.4.8  Material sublet **

A material lot may be stored in separately identifiable quantities. Each separately identifiable quantity of the same material lot shall be presented as a material sublet. All material sublots are part of the same material lot, so they have the material lops property values. A material sublot may be just a single item. Table 29 lists the attributes of material sublot Material sublets rnay have sublot specific properties.

Material sublot properties may contain nested material sublet properties.

> EXAMPLE Sublot propertles may be RFID tag !Ds or other identification properties, such that each sublet of a lot has a different property value.

Each material sublet shall contain the location of the sublot and the quantity or amount of material available in the sublot.

Material sublots may contain other sublots.

> NOTE For example, a sublet may be a pallet, each box on the pallet may also be a sublot, a. each material blister pack in the box may also be a sublet

A material sublot shall include

a\) a unique identification of the sublot,

b\) the storage location of the sublet;

c\) the unit of measure of the material \(for example, parts, kg, tons\);

d\) any status of the sublot.

**Table 29 — Attributes of material sublet **

|  | Description | Production Examples | Maintenance Examples | Qanlity Examples | inventory examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique Identification of a specific material sublot, within the scope of the information exchanged \(prodcution capability, production schedule, production performance ...\) &lt;br /&gt;The ID shall be used in other parts of the model when the material sublot need to be identified, such as the production capability for this material sublot, or a production response indetifying the material sublot used. | 1999-10-27- a67-B6653 | L8828-81-S1 | L53920-02-A554 | L8262-33-2 |
| Description | Additional information about the material sublot | Pallet 2 of 6 | oil | Reagent | wraping  material |
| Assembly Type | Optional: Defines the type assembly. The defined types are:&lt;br /&gt;Physical - The components of the assembly are physically connected or in the same area | Physical | Physical | Logical | Physical |
| Assembly Relationship | Optional: Defines the type of the relationships. The defined types are: &lt;br /&gt;Permanent — An assembly that is not intended to spilt during the production process.&lt;br /&gt;Transient — A temporary assembly using during production, such as a pallet of different materials pr a batch kit.&lt;br /&gt;Note 2 If material lost \(or sublots\) are merged or absorbed \(e.g. blended\), then this is a new material lot, as defined in Part 1 of this standard, not an assembly | Permanent | Transient | Permanent | Transient |
| Status | Status of the material lot. For example, released, approved, blocked, in process, in quality check. | Released | approved | blocked | approved |
| Storage Location | An identification of the storage location or a physical location of the material sublot | Stainless Steel Tote \#57 | Maintenance Shed 4S, Top Sheft | Work Bench 10, Top SHelt | Warehouse 1 |
| Quantity | The quantity of the material sublot | 40 | 10 | 1 | 41 |
| Quantity Unit of Measure | The unit of measure of the associated quantity, if applicable | sheets | cans | liter | rolls |

**5.4.9  Material test specification **

A representation of a material test shall be shown as a material test specification. A material test specification shall be associated with one or more material definition properties. This is typically used where a test is required to ensure that the material has the required property value. A material test specification rnay identify a test for one or more material definition properties. Not all properties need to have a defined material test specification. Table 30 lists the attributes of material test specification.

Material test specifications may also be related to a production request. The same material may have different specifications for different production requests, depending on specific customer requirements.

A material test specification shall include

a\) an identification of the test;

b\) a version of the test,

c\) a description of the test.

**Table 30 — Attributes of material test specification **

| Attribute Name | Description | Production examples | Maintenance | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of a test for certifying one or more values for one or more equipment properties.&lt;br /&gt;For example, this may be the name of a document that describes or lists the capability test. | STMT-101 | MI330 | QA8899 | 67 |
| Description | Additional information about the Material Test Soecification. | Sheet thickness measurement test - returns the average sheet thickness based on a sample plan and technique for a specific lot | Test of water content in an oil | Check of vendor's COA on pH | Check of vendor's COA for weight or wrapping material |
| Version | An identification of the version of the material Test Specification | 1.0 | 1.0 | 2.1 | A.1 |

**5.4.10 Material test result **

A representation of the results from the execution of a quality assurance test shall be presented as a material test result. A material test result records the results from a material test for a specific material lot or material sublet. The following are some characteristics of material test results. Table 31 lists the attributes of material test result.

a\) They shall be related to a material lot or material sublot.

b\) They may be related to a production request.

c\) They may be associated with a specific production response.

d\) They may be related to a specific process segment.

e\) They may include a pass/fail status of the test.

f\) They may include quantitative information of the tests.

g\) They may include the granting or refusing of an in-process or finished goods waiver request.

h\) They may be related to a product characteristic.

Material test results may be associated with a specific production response.

**Table 31 —Attributes of material test result **

| Attribute name | Description | Production Examples | Maintenance Examples | Quality Examples | inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique Instance identification that records the results from the execution of a test identified in a material test specification for a lot or sublot. \(For example, this may just be a number assigned by the testing authority \) | THK101/01-10-2000 | MO998 | 7763 | u7373 |
| Description | Additional information about the MNaterial Test Result. | Results from thickness test for PlastiFab lot on 1999-10-25 | Test of metal content in oil | Test of water pH | check of expiration date |
| Date | The date of the material test | 1999-10-25 11:30 | 2008-01-23 | 2008-01-20 | 2008-01-23 |
| Result | The value or list of values the returned from the performance of the material test. For example: Pass, Fail, 95, Red, Green | Pass | 20 | 6.9 | Pass |
| Result Unit of Measure | The unit of measure of the associated test result, if applicable | &lt;Pass, Fail&gt; | ppm | pH | &lt;Pass, Fail&gt; |

**5.4.11 Assemblies **

Assemblies are collections or sets of related elements. Assemblies are represented as relationships between elements and attributes of the elements. Each assembly element has its own identity and properties, such as a material lot which has its own identity and properties. An object with an assembly \(material lot, material sublot, material class, and material definition\) is contains the list of other elements that make up the assembly.

> NOTE 1 Many assembly type industries, such as automobile manufacturing, airplane assembly, and hftnibfte manufacturing use the concept of assemblies. A produced matenal, a unique identlfication and properties, is made up of other materials with their own unique identificatbn a. propertles.
>
> EXAMPLE 1 An 'automobile' is a material lot, with spear. properties \(co.r, VIN \#, make, model, ...\) while it also contalns other chassis parts \(engine, transmission, axles ...\) that also have their own unique Identification and properties.
>
> EXAMPLE 2 A transaxie In an automobile has Its own identification a. also is an assembly of subcomponents, as shown in Figure X, including seals, bearing, axle shaft, etc, as shown in Figure 10. There may be an assembly whIch defines a specific model of transmission described in a Material Dermition Assembly,
>
> EXAMPLE 3 A 'batch kit" is an assembly that contains a collection of different materials that would be used in the productbn of a batch, for example a batch kit for a soup may contain the seasonings that are used in production of a single bat. There may be an assembly which defines the class of materials used in a batch kit described in a Material Class Assembly, and there may be a batch specific assembly which defines specific material lots or sublets descnbed in a Material Assembly.

![](/assets/F-10.png)

**Figure 10 — Example of a material with an assembly **

