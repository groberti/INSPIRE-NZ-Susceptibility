# INSPIRE-NaturalRiskZone-SusceptibilityExtension
We present an extension to the INSPIRE Natural Risk Zone Schema to include Susceptibility Area as a feature type. Susceptibility is the relative spatial probability of occurrence of a specific type of hazard, based on intrinsic variables of an area (SafeLand 2011). The concept of susceptibility differs from the concept hazard in that the temporal probability of occurrence, the triggering factors, and the magnitude of the event are not considered in the definition of a susceptibility map (SafeLand 2011, Van Den Eeckhault 2012).
The term “susceptibility” is mentioned in the INSPIRE data specifications for Natural Risk Zones, yet the concept is not implemented as a feature type. The Extension to include Susceptibility Area is based on the [Natural Risk Zones Core Schema](https://inspire.ec.europa.eu/schemas/nz-core/4.0/). Two Feature Types have been added to the Core schema; 
*  [Abstract Susceptibility Area](http://minerva.codes/featureconcept/AbstractSusceptibilityArea)
*  [Susceptibility Area](http://minerva.codes/featureconcept/SusceptibilityArea)

## Data structure
The Susceptibility area feature type schema structure is modeled on Hazard Area and Risk Zone Feature types in the Natural Risk Zone core schema. Susceptibility Area is similar to Hazard Area in structure, and it differs from it by including the elements Influencing Factor and Relative Spatial Likelihood of Occurrence. Influencing Factor is defined, following SafeLand (2011) recommendation, as the intrinsic, preparatory variables which make an area susceptible to a hazard. Influencing factors are unbounded in multiplicity and can be defined qualitatively or quantitatively. Qualitative Influencing Factors are expressed as a string, while Quantitative Influencing Factors are GML:MeasureType. Whether defined Quantitatively or Qualitatively the Influencing Factor can also define a DataSet Type attribute, such as Slope or Air Quality. Influencing Factor allows end users of the Susceptibility Area datasets to understand which known conditions of that area resulted in the calculation of that Relative Spatial Likelihood of Occurrence.  Relative Spatial Likelihood of Occurrence element can be Quantitatively or Qualitatively defined. It is defined as values representing the spatial probability of occurrence of a specific hazard type, given the Influencing Factors present in the area (SafeLand 2011). 

## Useful Links 

[Natural Hazard Category Varnes Landslide Extension](http://minerva.codes/codelist/NaturalHazardCategoryValue) For applications in Landslide susceptibility we suggest using this INSPIRE codelist extension for describing *typeOfHazard*

[Veneto Landslide Susceptibility Map](https://map.italy.minervageohazards.com/) Example application of this extension in practice. 

## Usage
This schema extension can be used with ETL tools to align hazard susceptibily maps and databases. The XSD schema has been tested with [Hale Studio](https://www.wetransform.to/products/halestudio/). 

## Acknowledgments
This schema extension has been developed by [Minerva Intelligence Inc.] (https://www.minervaintelligence.com/) as a part of the INSPIRE Helsinki 2019 Data Challenge. 
