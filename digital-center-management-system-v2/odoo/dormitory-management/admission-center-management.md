# Admission Center management

In order to manage centers you need to have OeHealth / Center manager user group assigned\
Center manager maintains list of Rehabilitation centers, Buildings, Wards and Beds, Options and other\
data related to Accomodation Center Management

**Data models**

**·       Centers options**

\
Menu access : OeHospital -> Configurations -> OeHFieldOptions -> Options\
Contains general list of available options for centers. Can be extended per needs.\
Fields:

* Name or Code - one of those should be field populated.
* Option type - use "Accomomdation Center options" (other types will be described on usage)
* Related product - not needed, unless invoicing is used ( usage explained under Invoicing)
* Name construct - How the name for this option will be displayed in user interface\
  \- (available options: Name, Code, Code - Name )\
  \- also possible to add other construct options

\- Options selected as available on Center will be propagated as options to building\
\- Options selected as available on Building will be propagated as options to Ward\
\- Options selected as acailable on Ward will be available as attributes/ options on Bed

**·       Rehabilitation Centers**

Menu access : OeHospital -> Management -> CenterManagement -> Centers\
Fields:

*
  * Related partner - usualy same partner as the main comapny partner, but also can use other partner ( like contact address of main partner or any other)
  * Name - name of center ( used on this vertical )
  * Code - code for this center (unique, used to generate BED code)
  * Gender - Used to enforce Gender selection on entity. Propagation of this selection is applied to all subordinate objects, in a way that Unisex accepts any gender, and Male/Female only accept/allow that gender for SU admission
  * Admission sequence - Sequence used to assign numbers to confirmed admissions.\
    \- sequence can be set on any submodel (building, ward, bed) if needed.

o   Options: Select options that are available in this Center\
Only selected options will be visible on Building as options to select

**·       Center Building**

Menu access : OeHospital -> Management -> CenterManagement -> Buildings\
Fields:

* Center - select center this Building belongs to. Also will apply selected otions available. If no options are activated on selected Center the Options tab is not visible at all.
* Name - name of building
* Code - code for this Building (unique, used to generate BED code)
* Gender
* Sequence - can be left unselected if set on center, in case of need for separating enumeration of addmision

**·       Ward**

Menu access : OeHospital -> Management -> CenterManagement -> Wards\
Fields

**·       Bed**

Menu access : OeHospital -> Management -> CenterManagement -> Bed\
Fields:\
<br>

*
  * Code
  * Ward
  * Gender

&#x20;
