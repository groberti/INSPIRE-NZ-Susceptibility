# INSPIRE-NaturalRiskZone-SusceptibilityExtension
Natural Risk Zone susceptibility Extension is an INSPIRE XML schema extension to include Susceptibility Area as a feature type. Susceptibility is the relative spatial probability of occurrence of a specific type of hazard, based on intrinsic variables of an area (SafeLand 2011). The concept of susceptibility differs from the concept hazard in that the temporal probability of occurrence, the triggering factors, and the magnitude of the event are not considered in the definition of a susceptibility map (SafeLand 2011, Van Den Eeckhault 2012).
The term “susceptibility” is mentioned in the INSPIRE data specifications for Natural Risk Zones, yet the concept is not implemented as a feature type. The Extension to include Susceptibility Area is based on the [Natural Risk Zones Core Schema](https://inspire.ec.europa.eu/schemas/nz-core/4.0/). Two Feature Types have been added to the Core schema; 
*  [Abstract Susceptibility Area](http://minerva.codes/featureconcept/AbstractSusceptibilityArea)
*  [Susceptibility Area](http://minerva.codes/featureconcept/SusceptibilityArea)

## Data structure
The Susceptibility Area feature type schema is modeled following the structure of Hazard Area and Risk Zone feature types in the Natural Risk Zone Core schema. Susceptibility Area has three elements geometry, Influencing Factor and Relative Spatial Likelihood of Occurrence. Influencing Factor is defined, following SafeLand (2011) as the intrinsic, preparatory variables which make an area susceptible to a hazard. Influencing factors are unbounded in multiplicity and can be defined qualitatively or quantitatively. Qualitative Influencing Factors are expressed as a string, while Quantitative Influencing Factors are GML:MeasureType. Whether defined Quantitatively or Qualitatively, the Influencing Factor can also define a DataSet Type attribute, such as Slope or Air Quality. Influencing Factor are used in the calculation of Relative Spatial Likelihood of Occurrence. Relative Spatial Likelihood of Occurrence element can be Quantitatively or Qualitatively defined. Following SafeLand (2011), Relative Spatial Likelihood of Occurrence are values representing the spatial probability of occurrence of a specific hazard type, given the Influencing Factors present in the area. Influencing Factor feature types allow end users of Susceptibility Area datasets to understand which known conditions of the specific area resulted in the calculation of that Relative Spatial Likelihood of Occurrence.  

## Useful Links 

For landslide susceptibility mapping applications we suggest using the INSPIRE codelist extension [Natural Hazard Category Varnes Landslide Extension](http://minerva.codes/codelist/NaturalHazardCategoryValue) for describing *typeOfHazard* schema Element

A practical example of the application of The Susceptibility Area Natural Risk Zone schema extension is this [Veneto Landslide Susceptibility Map](https://map.italy.minervageohazards.com/)

## Usage
This schema extension can be used with ETL tools to align hazard susceptibily maps and databases. The XSD schema has been tested with [Hale Studio](https://www.wetransform.to/products/halestudio/). When importing this as a target schema in hale studio it is recommended to edit mappable types such that the Natural Risk Zone core schema is also available. 

## Acknowledgments
This schema extension has been developed by [Minerva Intelligence Inc.] (https://www.minervaintelligence.com/) as a part of the INSPIRE Helsinki 2019 Data Challenge. git 