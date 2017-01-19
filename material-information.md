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
|  |  |  |  |  |  |

A material class may be defined as containing an assembly of material classes and as part of an assembly of material classes: 

1. A material class rnay define an assembly of zero or more material classes. 
2. A material class rnay be an assembly element 00 0000 or more material classes. 
3. An assembly may be defined as a permanent or transient assembly of material classes. 
4. An assembly may be defined as physical or a logical assembly of material classes. 

**5.4.3  Material class property **

Properties of a material class shall be presented as material class properties. A material class shall be further characterized through zero or more material class properties. Table 24 lists the attributes of material class property. A material class properly may be tested by the execution of a material test specification. 

