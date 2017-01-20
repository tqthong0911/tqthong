**5.5.1 Process segment model **

Process segments are the smallest elements of manufacturing activities that are visible to business processes. The process segment model is a hierarchical model, in which multiple levels of abstraction of manufacturing processes may be defined because there may be multiple business processes requiring visibility to manufacturing activities.

> NOTE The term business provess segment Is a synonym for process segment a. Is used to reflect the business process aspect of the process segment.

Process segments are also logical grouping of personnel resources, equipment resources, and material required to perform a manufacturing operations step. A process segment defines the needed classes of personnel, equipment, and material, and/or it may define specific resources, such as specific equipment needed. A process segment may define the quantity of the resource needed.

The manufacturing operations step may be a production operations step, inventory operations step, maintenance operations step, and quality operations step.

Figure 11 is the process segment model. ![](/assets/F-11.png)

**Figure 11 — Process segment model **

**5.5.2 Process segment attributes **

A process segment lists the classes of personnel, equipment, physical assets, and material needed, and/or it may present specific resources, such as specific equipment needed for the process segment. A process segment may list the quantity of the resource needed.

A process segment is something that occurs or can occur during manufacturing operations.

Process segment may identify

a\) the time duration associated with the resource;

> NOTE Five hours or 5 hours/100 kg

b\) constraint rules associated with ordering or sequencing of segments.

A process segment may be made up of other process segments, in a hierarchy of definitions.

Process segments may contain specifications of specific resources required by the Process segment Process segments may contain parameters that can be listed in specific operations requests.

**Table 32 defines the attributes for process segment objects. **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examplea | inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique identification of a process segment, within the scope of the information exchanged \(operations capability, operations schedule, operations performance .\)&lt;br /&gt;The ID shall be used in other parts of the model when the process segment needs to be identified, such as the operations capability for this segment, or an operations response Identifying the segment. | Widget Frame Milling | Replace Motor | Pull Sample and Run Test | Transfer |
| Description | Additional InformatIon about the process segment. | Frame milling operation, separately costed operation | Large size motor replacement | Check purity and concentrat ion | Move pallet from truck to conveyor system |
| Operations type | Describes the category of the activity&lt;br /&gt;Required attribute.&lt;br /&gt;Defined values are: Production, Maintenance, Quallty, inventory, or mixed&lt;br /&gt;'Mixed' shall be used when the activity contains several categories of process segments | Production | Maintenance | Quality | inventory |
| Hierarchy Scope | identifies where the exchanged information fits within the role based equipment hierarchy.&lt;br /&gt; Optionally defines the scope of the process segment definition, such as the site or area it is defined for. | South Shore \(Site\)/ Work Line \(Area\) | South shore \(SITE\)/ Packaging \(Area\) | Mixer Sample Port \(Work Unit\) | Receiving dock \(work Center\) |
| Duration | Duration of process segment, if known | 25 | \(not applicable\) | 20 | 5 |
| Duration Unit of Measure | The units of measure of the duration, if defined | Minutes | \(not applicable\) | minutes | minutes |

**5.5.3  Personnel segment specification **

Personnel resources that are required for a process segment shall be presented as personnel segment specifications.

** Table 33 defines the attributes for personnel segment specification objects. **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Personnel Class | Identifies the associated personnel class of set of personnel classes specified | Milling Machine Operator | Type 2 Mechanic | Lab Tech A | Lift truck operator |
| Person \* | Identifies the associated person or set of persons specified | &lt;n/a&gt; | &lt;n/a&gt; | &lt;n/a&gt; | &lt;n/a&gt; |
| Description | Contains additional information and descriptions of the personnel segment specification definition. | Defines the time for journey man milling machine operators for each widget frame milling process segment. | Qualified to replace motor type NEMA 4. | Quanlified to operation of reflectometer | Certified lift truck operator |
| Personnel Use | Defines the expected use of the personnel class or person. | Allocated | Certified | Certified | Allocated |
| Quantity | Specifies the personnel resource required for the parent process segment, if appliacble | 1.3 | 2 | .5 | 5 |
| Quantity Unit of Measure | The unit of measure of the associated quantity, if applicable | Hours / piece | Hours / motor | Hours / sample | minites / transfer |

> Note Typically only personnel class is defined

**5.5.4 Personnel segment specification property**

Specific properties that are required are specified in personnel segment specification properties. Personnel segment specification properties may contain nested personnel segment specification properties.

Table 34 defines the attributes for personnel segment specification property objects

**Table 34 — Attributes of personnel segment specification property **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | inventory examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of a property of the associated person properly or personnel class property. | Height | Scuba Trained | Color Vision | 2^nd Shift |
| Description | Contains additional information and descriptions of the property. | Defines the required minimum height of a milling machine operator | Class 4 work requires use of scuba underwater | Must distinguish red and green | Must be able to operate 2^nd shift |
| Value | The value, set of values, or range of the property. | 150 | TRUE | TRUE | TRUE |
| Value Unit of Measure | The unit of measure of the associated property value, if applicable. | cm | &lt;True, False&gt; | &lt;True, False&gt; | &lt;True, False&gt; |
| Quantity | Specifies the personnel resource required, if applicable | 1.3 | \(not applicable\) | \(not applicable\) | \(not applicable\) |
| Quantity Unit of Measure | The unit of measure of the assoclated quantity, it applicable, | Hlours / piece | \(not applicable\) | \(not applicable\) | \(not applicable\) |

**5.5.5 Equipment segment specification **

Equipment resources that are required for a process segment shall be presented as equipment segment specifications.

Table 35 defines the attributes for equipment segment specification objects.

**Table 35 — Attributes of equipment segment specification **

| Attribute Name | Description | Production Examples | MainMnance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Equipment Class | Identifies the associated equipment ctass or set of equipment classes of the capability. | \(not applicable\) | 10 Ton Crane | Reflectometer | 800 KG Fork Truck |
| Equipment \* | Identifies the associated equipment or set of equipment of the capability. | Milling Machine 001 | \(not applicable\) | \(not applicable\) | \(not applicable\) |
| Description | Contains additional information and descriptions. | Equipment need for widget milling process segment | Crane reuired to remove motor | Measures substrate thickness of wafer | Able to lift two standard pallets |
| Equipment use | Defines the expected use of the equipment class or equipment in the context of the process segment. | Part Milling | Remove and Replace Motor | Run test | Material Movement |
| Quantity | specifies the amount of resources required, if applicable | 1.3 | 1 | 1 | 1 |
| Quantity Unit of Measure | The unit of measure of the associated quantity, if applicable. | Machine Hours / piece | Day | Test | Move |

NOTE Typically either equipment Wass or equipment Is defined

**5.5.6 Equipment segment specification property **

Specific properties that are required are specified in equipment segment specification properties.

Equipment segment specification properties may contain nested equipment segment specification properties.

Table 36 defines the attributes for equipment segment spec fication property objects.

**Table 36 — Attributes of equipment segment specification property **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An Identification of a property of the associated equipment property or equipment class property | Milling Direction | Molbile | calibrated | Power |
| Description | Contains additional information and descriptions | Only vertical milling machines are suitable for wldget milling. | Mobile crane | Within calibrated date | Type of power |
| Value | The value, set of values, or range of the property, For example: vertical, Horizontal | Vertical | TRUE | TRUE | Electric |
| Value Unit of Measure | The unit of measure of the associated property value, If applicable, | \(not applicable\) | &lt;True. False&gt; | &lt;True. False&gt; | {Electric, Gas, LP} |
| Quantity | Specifies the amount of resources required. | 1.0 | \(not applicable\) | \(not applicable\) | \(not applicable\) |
| Quantity Unit of Measure | The unit of measure of the associated quantity, if applicable. | Machine Hours / Piece | \(not applicable\) | \(not applicable\) | \(not applicable\) |

**5.5.7 Material segment specification **

Material resources that are required fora process segment shall be listed as material segment specifications.

Table 37 defines the attributes for material segment specification objects.

**Table 37 — Attributes of material segment specification **

| Attribute Name | Description | Production Examples | Maintenanc Examples | Quality Examples | inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Material Class | Identifies the associated material class or set of malarial classes of the capability • | Polymer sheet stock 1001A | Motor Brushes | Sample Holder | Pallet |
| Material Definition | Identifies the associated material definition or set of material definitions of the capability • | Sheet stock 1443a | \#9949 | Polyurethane sample holder | Plastic Pallet |
| Description | Contains additional information and descriptions | Defines the polymer reuired for a widget milling process segment | Brushes required during motor maintenance | Disposable sample holder | Pallet used for storage |
| Assembly Type | Optional: Defines the type of the assembly The defined types are:&lt;br /&gt; Physical — The components of the assembly are physically connected or in the same area.&lt;br /&gt;Logical— The components of the assembly same area physical connected or in the same area. | Physical | Physical | Logical | Physical |
| Assembly Relationship | Optional: Defines the type of the relationships. The defined types are:&lt;br /&gt; Permanent —An assembly that is not intended to be spilt during the production process.&lt;br /&gt;Transient — A temporary assembly using during production, such as a pallet of different materials or a batch kit. | Material Consumed | Material Consumed | Material Consumed | Material Consumed |
| Material Use | Defines the materlal use.&lt;br /&gt; For production defined values are: Consumable, Material Produced | Material Consumed | Material Consumed | Material Consumed | Material Consumed |
| Quantity | Specifies the arnount of resources required | 0.35 | 6 | 1 | \(not applicable\) |
| Quantity Unit of Measure | The unit of measure of the associated property value, if applicable | Sheets / piece | Units | Units | \(not applicable\) |

> Note \* Typically either a material class or material definition is specified.

A material segment specification may be defined as containing an assembly of material segment specifications and as part of an assembly of material segment specifications:

1. A material segment specification may define an assembly of zero or more material segment specifications. 
2. A material segment specification may be an assembly element of zero or more material segment specifications. 
3. An assembly may be defined as a permanent or transient assembly of material segment specifications. 
4. An assembly may be defined as physical or a logical assembly of material segment specifications. 

**5.5.8 Material segment specification property**

Specific properties that are required are specified in material segment specification properties. Material segment specification properties may contain nested material segment specification properties.

Table 38 defines the attributes for material segment specification property objects.

**Table 38 — Attributes of material segment specification property**

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of a property of the associated material properly or equipment class property. | Average Surface Roughness | 314 Stainless steel | sterilized | REID |
| Description | Contains additional information and descriptions | Defines the minimum polyethylene roughness quality, | Required alloy | Sterilized sample holder | Pallet contains an active RFID |
| Value | The value, set of values, or range of the property. | 66.748 | TRUE | TRUE | Active |
| Value Unit of Measure | The unit of measure of the associated property value, if applicable. | Angstroms | &lt;True, False&gt; | &lt;True, False&gt; | &lt; Active, Passive, Noe&gt; |
| Quantity | Specilles the amount of resources required, if applicable. | 0.10 | \(not applicable\) | \(not applicable\) | \(not applicable\) |
| Quantity Unit of Measure | The unit of measure of the associated property value, if applicable. | Sheets /piece | \(not applicable\) | \(not applicable\) | \(not applicable\) |

**5.5.9 Physical asset segment specification**

Physical asset resources that are required tore process segment shall be presented as physical asset segment specifications.

Table 39 defines the attributes for physical asset segment specification objects.

**Table 39 — Attributes of physical asset segment specification **

| Attribute name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Physical Asset Class | Identifies the associated physical asset class or set of physical asset classes of the capability | Acme Super TT10 | Easy bake 1969 | Wafes R Us RF 100 | SupperTote 2000 |
| Physical Asset | Identifies the associated physical asset or set of ophysical assets of the capability | Tl-101 | OV-1200 | RF-140 | Tote 12A |
| Description | Contains additional information and descriptions. | Temperature of granulation process | Preventive maintenance | thickness measurement | Storage |

Description

**5.5.10 Physical asset segment specification property **

Specific properties that are required are specified in physical asset segment specification properties.

Physical asset segment specification properti may contain nested physical asset segment specification properties.

Table 42 defines the attributes for physical asset segment specification property objects.

**Table 40 — Attributes of physical asset segment specification roperty **

| Attribute Name |  Description |  Production Examples |  Maintenance Examples | Quality Examples |  inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identlfMation of a property of the assoclated physical asset property or physical asset class property | temperature calibration date | Run clock | Calibrated | Tote Type |
| Description | Contains additional information and descriptions calibration  | Calibration date no later than 6 months from use | Running time hours from last preventive maintenance |  Within calibrated date | Only plastic totes |
| Value | The value, set of values, or range of the property For example: Vertical, Horizontal | 1999-12-31 | 1200 | True | Plastic |
| Value | Unit of Measure The unit of measure of the associated property value, if applicable | Date | Hours | &lt;True, False&gt; | String |
| Quantity | Specifies the amount of resources required | \(not applicable\) | \(not applicable\) | \(not applicable\) | 3 |
| Quantity Unit of Measure | The unit of measure of the associated quantity, if applicable  | \(not applicable\) | \(not applicable\) | \(not applicable\) | Count |

**5.5.11 Process segment parameter **

Specific parameters required for a segment shall be shown as process segment parameters. Process segment parameters may contain nested process segment parameters. Table 41 defines the attributes for process segment parameter objects. 

**Table 41 — Attributes of process segment parameter **

| Attribute Name | Description |  Production Examples |  Maintenance Examples | Quality Examples |  inventory Example• |
| :--- | :--- | :--- | :--- | :--- | :--- |
|  ID | identification of the process segment parameter,  | Milling Time | Crane Lead Time |  Sample Size |  Number of Pallets |
|  Description | Contains additional information.  | Range of acceptable milling times | Known lead time to get crane available | Size of sample to be pulled | Number of pallets needed for move |
| Value | The value, set of values, or range of acceptable values | {5..10} | {1..20} | {5-20} | \(not applicable\) |
| Unit of Measure  | Unit of measure of the values, if applicable | Minutes | Days | mg | \(not applicable\) |

**5.5.12 Process segment dependency **

Table 42 defines the attributes for process segment dependency objects. The process segment dependencies can be used to describe process dependencies that are independent of any particular product or operations task. 

| Attribute Name |  Description |  Production Examples |  Maintenance Examples | Quality Examples |  inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | The identification of the unique instance of the process segment dependency. | PSD001 |  34 |  A35 |  PSA.I-5583 |
| Description |  Contains additional information and descriptions of the process segment dependency definition. | Defines the dependency definition of assembly processes the Widget Assembly process segmegment | Don't start until production is complete  | May pull samples anytime during production | Don't move to storage released by qualily |
| Dependency Type | Defines the execution dependency constraints of one segment by another segment | Start Cleanout no earlier than T \(Timing Factor\) after work end | Start motor Replacement after Cleanout end | Pull Sample may run in parallel with MIX | Move Inventory after Quality Release |
| Dependency Factor | Factor used by dependency |  25 | \(not applicable\) | \(not applicable\) | \(not applicable\) |
| Unit of Measure | The units of measure of the dependency factor, if defined |  Minutes |  \(not applicable\)  |  \(not applicable\)  |  \(not applicable\)  |

EXAMPLE Using 'A' and 'B' to identify the process segments,or specific resources within, the segments, and T to identify the timing fator as shown in Figure 12, the dependencies include 

* B can not follow A 
* B may run in parallel to A 
* B may not run in parallel to A 
* Start B at A start 
* Start B after A start 
* Start B after A end 
* Start B no later than T \(Dependency Factor with tune T\) after A start 
* Start B no earlier than T \(Dependency FaMor with time T\) after A start 
* Start B no later than T \(Dependency Factor with tune T\) after A end 
* Start B no earlier than T \(Dependency FaMor with time T\) after A end 



