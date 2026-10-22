## objects
### person
* name
*	gender
*	date of birth
*	place of birth 
*	date of death
*   place of death 
*	nationality / country of origin
*	family background 
*	archaeological field
*	main occupation

### family background
*	mother's occupation 
*	father's occupation
*	notable relatives 
*	notes

### organization
*	name
*	type (university, museum, excavation institute, research council etc.)
*	headquarters 
*	date of foundation
*	date of dissolution (if applicable)
*	country

### geo_place
*	name (and historical names)
*	type (city, region, country, excavation site, etc.)
*	longitude
*	latitude
*	country (at the time)

### publication
*	bibliographic reference
*	title
*	type (monograph, article, excavation report, etc.)
*	year of publication
*	place of publication 
*	publisher / journal

### role_in_publ
* 	role

### excavation
*	title of the excavation or project
*	site
*	type (excavation, survey, rescue excavation, etc.)
*	start year
*	end year
*	period
*	directing organization 
*	notes

### field
*	name (prehistory, classical archaeology, near-eastern archaeology etc.)

### education
*	organization (university, school, institute)
*	place
*	subject / field
*	degree 
*	start year
*   end year

### employment
*	organization
*	place
*	position / role /title (curator, professor, field director)
*	start year
*	end year

### membership
*	organization
*	place
*	role (member, board member, president, etc.)
*	year of joining
*	year of leaving

### excavation participation
*	excavation
*	role (director, field director, assistant, specialist, student, etc.)
*	start year
*	end year

## Relations between objects
*	person was born in geo_place
*	person died in geo_place
*	person comes from family background
*	person is a student of person (teacher-student relation, with years)
*	person studied at organization (via Education, with years and place)
*	person was employed by organization (via Employment, with years and place)
*	person is a member of organization (via Membership, with years and place)
*	person took part in excavation (via Excavation Participation, with role and years)
*	excavation took place at geo_place
*	excavation was carried out by organization
*	publication reports on excavation
*	person works in field
*	publication has as place of publication place
*	publication was published in year
*	organization is headquartered in geo_place
*	organization was founded in geo_place and year
*	person collaborated with person (joint excavations, co-authors)
*	person is related to person (family ties within the field)
*	organization is part of organization (for example institute within a university)
* publictaion cites publication
* 	person has a role_in_publ in publication
