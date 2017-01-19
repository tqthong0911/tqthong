**5.1.1 Personnel model **

The personnel model shown in Figure 5 contains the information about specific personnel, classes at personnel, and qualifications at personnel.

![](/assets/import.png)

**5.1.2 Personnel class**

A personnel class is a representation of a grouping of persons with similar characteristics for a definite purpose such as manufacturing operations definition, scheduling, capability and performance. Any person may be a member of zero armors personnel classes. Table 4 lists the attributes of personnel class. A personnel class may be tested by the execution of a qualification test specification.

NOTE Examples of personnel classes are cook machine mechanics, slicing machine operators, cat-cracker operator, and zipper line inspectors\_

**Table 4 — Attributes of personnel class**

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique identification of a specific personnel class. These are not necessarily job titles, but identify classes that are referenced in other parts of the model. | Widget Assembly Operator | Maintenance Technician Grade 1 | Snior Lab Assistant | Warehouse Manager |
| Description | Additional information and description about the personnel class. | General information about widget assembly operators. | Highest grade for maintenance technician | Highest level of lab assistants | Person responsible for the warehose |

EXAMPLE: A personnel class may be assoclat d to a qualification test specification MMout reference o a property, such as a qualification test specIfIc tion for a Mrt truck operator, in Mac the lest deterrni ad if the person Is a member of the class of Mrk truck operators.

**5.1.3  Personnel class property**

Properties of a personnel class shall be shown as personnel class properties. Each personnel class shall have zero or more recognized properties. Table 5 lists the attributes of personnel class property.

NOTE Examples of personnel class properties Mr the personnel class operators are class I certified, class 2 certified, night shift, and exposure hours.

Production requests may specify required personnel class property requirements fore product segment.

A personnel class property may be tested by the execution of a qualification test specification.

Personnel class properties may contain nested personnel class properties.

**Table 5 — Attributes of personnel class property**

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An indentification of the specific property, unique under the scope of the parent personnel class object.   &lt;br/&gt;For example the property "Has class 1 safety Training" \(with values of Yes or No\) may be defined under several defferent Personnel Class definitions, such as Fork Lift Operator and Pipe Fitter classes, but has a different meaning for each class. | Class 1 Certified | Electrician Skills Class | LGC Model 1003 Certified Operator | List Truck Driver |
| Description | Additional information and description about the personnel class property. | Indicates the certification level of the operator. | Level of Skill Attained | Indicates if qualified to run equipment | Indicates if allowed to drive lift trucks. |
| Value | The value, set of values, or range of the property. &lt;br/&gt;This presents a range of possible numeric values, a list of possible values, or it may be empty if any value is valid. | &lt;True, False&gt; | &lt;Master, Journeyman, Apprentice&gt; | &lt;True, False&gt; | &lt;True, False&gt; |
| Value Unit of Measure | The unit of measure of the associated property values, if applicable. | Boolean | String | Boolean | Boolean |

**5.1.4 Person**

A person is a representation of a specifically identified individual. A person may be a rnember of zero or more personnel classes. Table 6 lists the attributes of person. A person may be tested by the execution of a qualification test specification.

Person shall include a unique identification of the individual.

**Table 6— Attributes of person **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | Aunique indentification of a specific person, within the scope of the information exchanged \(production capability, production schedule, production performance, .....\)&lt;br/&gt;The ID shall be used in other parts of the model when the person needs to be identified such as the production capability for this person, or a production response indentifying the person. | Employee 23 | 22828 | 999-123-4657 | 007 |
| Description | Additional information about the resource. | Person Information | Maintenance Tech | Lab Tech | Driver |
| Name | The name of the individual.&lt;br/?This is meant as an additional identification of the resource, but only as information and not as a unique value. | Jane | Jim | John | James |

**5.1.5  Person property **

Properties of a person shall be listed as person properties. Each person shall have zero or more person properties. These specify the current property values of the person for the associated personnel class property. Table 7 lists the attributes of person property.

NOTE For example, a person properly may be night shift and its value would be available, a. a person properly may be exposure hours available and its value would be

Person properties may include the current availability of a person and other current information, such as location and assigned activity, and the unit of measure of the current information.

A person property may be tested by the execution of a qualification test specification with test results exchanged in a qualification test result.

Person properties may contain nested person properties.

**Table 7 — Attributes of person property **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of the specific property. | Exposure Hours Available | Union ID | LGC Model 1003 Certified Operator | Lift Truck Driver |
| Description | Additional information aboutthe person property. | Indicates number of exposire hours availables this month | Union ID number | indicates if qualified to run equipment | Indicates if allowed to drive lift trucks. |
| Name | The value, set of values, or range of the property&lt;br/&gt;The value\(s\) is assumed to be within the range or set of defined values for the related personnel class property. | 4 | CA55363 | true | False |
| Value Unit of Measure | The unit of measure of the associated property value, if applicable | Hours | string | Boolean | Boolean |

**5.1.6 Qualification test specification **

A representation of a qualification test shall be presented as a qualification test specification. A qualification test specification may be associated with a personnel class, a personnel class property, a person, or person property. This is typically used where a qualification test or properly demonstrated competency is required to ensure that a person has the correct training and/or experience for specific operations. A qualification test specification may test for one or mare properties. Table 8 lists the attributes of qualification test specification.

A qualification test specification shall include

a\) an identification of the test;

b\) aversion of the test;

c\) a description of the test.

**Tablet 8—Attributes of qualification test specification **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | An identification of a test for certifying one or more values for one or more person properties.&lt;br/&gt;For example, this may be the name of a document that describes or defines the qualification test. | Class 1 Widget Assembly Certification Test | Union Renewal Test | LGC model 1003 Certification Test | Fork Truck Driving Test |
| Description | Additional information and description about the qualification test specification. | Indentifies the test for Class 1 Widget assembly certification - returns a True or False value for the Class 1 widget assembly certification property | Renewal or union membership | Identifies test for correct operation of LGC Model 1003 | Identifies test for driving fork truck |
| Version | An identification of the version of the qualification test specification | V23 | 01 | A | 23C |

**5.1.7  Qualification test result **

The results from a qualification test for a specific person shall be given as a qualification test result. Table 9 lists the attributes of qualification test result

A qualification test result shall include

a\) the date of the test;

b\) the result of the test \(for example, passed or failed\);

c\) the expiration date of the qualification.



**Table 9 — Attributes of qualification test result **

| Attribute Name | Description | Production Examples | Maintenance Examples | Quality Examples | Inventory Examples |
| :--- | :--- | :--- | :--- | :--- | :--- |
| ID | A unique instance identification that records the results from the excution of a test identified in a qualification test specification for a specific person. \(For example, this may just be a number assigned by the testing authority\) | T5568700827 | UR20070809 | LGC55.3 | 77276 |
| Description | Additional information and description about the qualification test results. | Results from Joe's widget assembly qualification test for October 1999. | Renewal | Particle Analyzer SOP Test | Fork lift driver safety SOP test |
| Date | The date and time of the qualification test. | 1999-10-25 13:30 | 2007-08-09 | 2008-10-31 | 2002-01-30 |
| Result | The result of the qualification test. For example: Pass, Fail | Pass | Pass | Fail | Fail |
| Result Unit of Measure | The unit of measure of the associated test result, if applicable. | &lt;Pass, Fail&gt; | &lt;Pass, Fail&gt; | &lt;Pass, Fail&gt; | &lt;Pass, Fail&gt; |
| Expiration | The date of the expiration of the qualification | 2000-10-25 13:30 | 2008-08-09 | 2008-10-31 | \(not applicable\) |



