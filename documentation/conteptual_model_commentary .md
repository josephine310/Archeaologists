## person
* any archaeologist from the list, or a person linked to one
### properties
* it is an object class, persistent item
* name, gender, birth and death date (if applicable), nationality, main occupation
### relations
* person was born in one geo_place
* person died in one geo_place
* person comes from one family background
* person works in any number of fields
* person can have any number of education, employments, memberships, excavation participations, roles in publication, person relationships
## field
* an archaelogical field
* for example: prehistory, classical archaeology , egyptology
### properties
* it is an object class, persistent item
* name
### relations
* a person works in 0..n fields, a field has 0..n persons
* an education can be linked to one field
## geo_place
* any geophysical place (city, region, country, excavation site)
### properties
* name, longitude, latitude
* it is an object class, persitent item
### relations
* a place has one geo_place_type and =..n place appelations
* a place is located in place (links place to the larger place that contains it)
* historical places are places of the type historical place
## geo_place_type
* types of places (city, region, country, excavation site, historical place)
### properties
* it is vocabulary
* name 
* definition
### relations
* an appellation belongs to one geo_place, a place can have 0..n appellations
## organisation
* any form of institution, university, museum, excavation institute, research council
### properties
* it is an object class, persistent item
* name, foundation date, dissolution date (if applicable)
### relations
* an organisation has one organisation type
* an organisation has a headquater in one geo_place
* an organisation was founded in one geo_place
* an organisation can be part of a larger organisation
* an organisation can carry out excavations
## organisation_type
* types of organisations
* for example university, museum, excavation institutes...
### properties
* it is vocabulary
* name, definition
### relations
* an organisation can have one organisation_type
## publication
* monograph, article, excavation report
### properties
* it is an object class, persistent item
* bibliographic reference, title, type, publication year, publisher
### relations
* a publication was published in at least one geo_place
* a publication can report on any number of excavations
* a publication has persons (role in publication)
## role_in_publication
* the role of a person in a publication
### properties
* it is a class, because a person can have several roles in a publication and a publication can have several persons
* it is a relationship class without dates
### relations
* one person and one publication
## excavation
* an excavation, survey, rescue excavation at one site (place)
### properties
* it is an object class, persistent item
* type, title, start and end date, period, notes
### releations
* an excavation takes place in one geo_place
* an excavation was carries out by at least one organisation
* an excavation has 0..n excavation-publications
* an excavation can be reported on by 0..n publications
## education
* a person studied at an organisation during a certain period
### properties
* temporal entity
* degree, start and end date
### realations
* one person and one organisation
* at least one geo-place and field
## employment
* one person held a position in an organisation for a certain period
### properties
* it is a temporal entity
* position, start and end date
### relations
* one person and one organisation, at least at one geo_place
* several employments are possible
## membership
* one person was or is a member of a organisation for a certain period
### properties
* it is a temporal entity
* role, start (and end) date
### relations
* one person and one organisation, at least at one geo_place
* multiple memberships are possible
## excavation_participation
* a person took part in an excavation with a role for a certain period of time
### properties
* it is a temporal entity
* role, start and end date
### relations
* one person and one excavation
## person_relationship
* a relationship between two persons (teacher-student, collabaration, family tie)
* the information about the parents would be found here
### properties
* it is a temporal entity
* start and end year, notes
### realations
* one person and another person
* one person_relationship_type
## person_relationship_type
* types of relationships
* family ties
### properties
* vocabulary
* name
## citizenship
* one person can have at least one citizenship
### properties
* temporal entity
### relations
* one person and one citizenship
