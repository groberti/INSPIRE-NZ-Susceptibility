# INSPIRE-NaturalRiskZone-SusceptibilityExtension
An extension to the INSPIRE Natural Risk Zone Schema to include Susceptibility Area as a feature type.  

Susceptibility is the spatial probability of natural hazard occurence.

The concept of susceptibility is mentioned in the INSPIRE data specifications for Natural Risk Zones, yet the concept is not implemented as a feature type. 
This Extension is based off the [Natural Risk Zones Core Schema ](https://inspire.ec.europa.eu/schemas/nz-core/4.0/). Two Feature Types have been added to the Core schema, [Abstract Susceptibility Area](http://minerva.codes/featureconcept/AbstractSusceptibilityArea) and [Susceptibility Area](minerva.codes/featureconcept/SusceptibilityArea).

## Data structure
The Susceptibility area feature type schema structure is modeled based on other feature types in the Natural Risk Zone core schema. Susceptibility Area is in fact very similair to hazard area in structure. Susceptibility Area has the element "Influencing Factor" this element differentiates it from Hazard Area. "Influencing Factor" is defined as *Known conditions of the area which influence the hazard susceptibility of the area.* it is unbounded in multiplicity and can be defined Qualitatively or Quantitatively. Whether defined Quantitatively or Qualitatively the element can also define a DataSet Type attribute. Influencing factor allows susceptibility area datsets to be self explanatory. When a Susceptibility Area feature is defined with a certain likelihood of occurence it is beneficial for the end user of the data to understand what known conditions of that feature resulted in the calculation of that likelihood. 

## Useful Links 

[Natural Hazard Category Varnes Landslide Extension](http://minerva.codes/codelist/NaturalHazardCategoryValue) For applications in Landslide susceptibility we suggest using this INSPIRE codelist extension for describing *typeOfHazard*
[Veneto Landslide Susceptibility Map](https://map.italy.minervageohazards.com/) Example application of this extension in practice. 

## Usage
This schema extension can be used with ETL tools to align hazard susceptibily maps and databases. The XSD schema has been tested with [Hale Studio](https://www.wetransform.to/products/halestudio/). 

## Acknowledgments
This schema extension has been developed by [Minerva Intelligence Inc.] (https://www.minervaintelligence.com/) as a part of the INSPIRE Helsinki 2019 Data Challenge. 
