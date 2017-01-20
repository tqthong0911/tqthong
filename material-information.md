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
| Assembly Type | Optional: Defines the type of the assembly. The defined types are: &lt;br /&gt;Physical - The compnents of the assembly are physically connected or in the same area.&lt;br /&gt;Logical - The components of the assembly are not necessarily physically connected or in the same area. | Physical | Physical  | Logical | Physical  |
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



| ID | Description | Production Examples | Maintenance Examples  | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
|  | A unique identification of a specific material definition, within the scope of the information exchanged \(production capability, production schedule, production performance,...\)&lt;br /&gt;The ID shall be used in other parts of the model when the material definition needs to be indentified, such as the production capability for this material definition, or a production response identifying the material definition used. | Sheet stock 1443a | DO200cpO | OA9929 | PW882929 |
| Description |  Additional information about the material definition | General purpose sheet stock |  200 cP Oil from Dino Oil | Oxidizing Agent from  RustitAil |  General purpose 20 mil wrap |
| Assembly Type  | Optional: Defines the type assembly. The defined types are:&lt;br /&gt;Physical - The components of the assembly are physically connected or in the same area | Physical | Physical | Logical | Physical |
| Assembly Relationship | Optional: Defines the type of the relationships. The defined types are: &lt;br /&gt;Permanent — An assembly that is not intended to spilt during the production process.&lt;br /&gt;Transient — A temporary assembly using during production, such as a pallet of different materials pr a batch kit. | Permanent | Transient | Permanent | Transient |

A material def nition may be defined as containing en assembly of material definitions and as part of an assembly of material definitions: 

1.  A material definition rnay define an assembly of zero or more material definitions. 
2. A mate ial definition may be an assembly element of zero or more material definitions. 
3. An as em Sly may be defined as a permanent or transient assembly of material definitions. 
4. An assembly may be defined as physical or a logical assembly of material definitions. 

**5.4.5  Material definition property **

Properties of a material definition shall be defined as material definition properties. A material definition shall be further characterized through zero or more material definition properties. 

Table 26 lists the attributes of material definition properly. A material definition property may be tested by the execution of a material test specification. 

Material definition properties may contain nested material definition properties. 

> NOTE Examples of material definition property Include density, pH factor, or material strength, Properties may present the nominal or standard values for the material. Table 26 — Attributes of material definition property

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



