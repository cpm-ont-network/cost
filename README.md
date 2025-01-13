Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# The Cost Item (CI) Ontology

## Metadata
* **IRI**
  * `http://w3id.org/ci`
* **Creators(s)**
  * [Cassandro, Jacopo](https://orcid.org/0000-0002-1487-8178)
    [[ORCID]](https://orcid.org/0000-0002-1487-8178)
    (<jacopo.cassandro@polimi.it></a>) of [Politecnico di Milano](https://www.dabc.polimi.it/persona/jacopo-cassandro/)
  * [Hagedorn, Philipp](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Politecnico di Milano](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Contributor(s)**
  * [Mirarchi, Claudio](https://orcid.org/0000-0002-9288-8662)
    [[ORCID]](https://orcid.org/0000-0002-9288-8662)
    (<claudio.mirarchi@polimi.it></a>) of [Politecnico di Milano, Dipartimento ABC](https://www.dabc.polimi.it/persona/claudio-mirarchi/)
  * [Sigalov, Katharina](https://orcid.org/0000-0002-3070-0759)
    [[ORCID]](https://orcid.org/0000-0002-3070-0759)
    (<katharina.sigalov@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/katharina_sigalov.html.en)
* **Created**
  * 2024-10-12
* **Modified**
  * 2025-01-13
* **Version Information**
  * 1.0
* **Imports**
  * [http://w3id.org/cr](http://w3id.org/cr)
  * [http://w3id.org/cterm](http://w3id.org/cterm)
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2025 by DABC, PoliMi
* **Ontology RDF**
  * RDF ([cost.ttl](turtle))
### Description
<p>The Cost Item (CI) Ontology is based on concepts and principles of construction project cost estimation an can be used together with the Construction Resources (CR) ontology and can use terminology from the Construction Terminology (CTERM).</p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Activity](#Activity),
[Construction Work](#ConstructionWork),
[CostComponent](#CostComponent),
[CostItem](#CostItem),
[Product Work](#ProductWork),
[ProductionResult](#ProductionResult),
[Temporary Work](#TemporaryWork),
[Work](#Work),
[WorkOfConstructionWork](#WorkOfConstructionWork),
[WorkOfProductWork](#WorkOfProductWork),
[WorkOfTemporaryWork](#WorkOfTemporaryWork),
### Activity
Property | Value
--- | ---
IRI | `https://w3id.org/ci#Activity`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfActivity](https://w3id.org/cterm#CategoryOfActivity) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **max** 5 [cterm:FunctionOfActivity](https://w3id.org/cterm#FunctionOfActivity) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:TemporaryComponent](https://w3id.org/ci#TemporaryComponent) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **max** 5 [cterm:UseOfActivity](https://w3id.org/cterm#UseOfActivity) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfActivity](https://w3id.org/cterm#ObjectOfActivity) (c)<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **max** 1 [cterm:TypeOfActivity](https://w3id.org/cterm#TypeOfActivity) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:LabourResource](https://w3id.org/cr#LabourResource) (c)<br />[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **max** 1<br />[ci:techSpecs](https://w3id.org/ci#techSpecs) (dp) **max** 1<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **exactly** 1 [cterm:FamilyOfActivity](https://w3id.org/cterm#FamilyOfActivity) (c)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
In domain of |[ci:keywords](https://w3id.org/ci#keywords) (dp)<br />[ci:techSpecs](https://w3id.org/ci#techSpecs) (dp)<br />[ci:code](https://w3id.org/ci#code) (dp)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op)<br />[ci:included](https://w3id.org/ci#included) (dp)<br />[ci:excluded](https://w3id.org/ci#excluded) (dp)<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op)<br />[ci:ActivityOf](https://w3id.org/ci#ActivityOf) (op)<br />
In range of |[ci:UnitOf](https://w3id.org/ci#UnitOf) (op)<br />[ci:SubComponentOf](https://w3id.org/ci#SubComponentOf) (op)<br />[ci:hasActivity](https://w3id.org/ci#hasActivity) (op)<br />
### Construction Work
Property | Value
--- | ---
IRI | `https://w3id.org/ci#ConstructionComponent`
Super-classes |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Restrictions |[ci:hasWork](https://w3id.org/ci#hasWork) (op) **exactly** 1 [ci:WorkOfConstructionComponent](https://w3id.org/ci#WorkOfConstructionComponent) (c)<br />
### CostComponent
Property | Value
--- | ---
IRI | `https://w3id.org/ci#CostComponent`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **exactly** 1 [cterm:FamilyOfCostComponent](https://w3id.org/cterm#FamilyOfCostComponent) (c)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfCostComponent](https://w3id.org/cterm#CategoryOfCostComponent) (c)<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[ci:PartOf](https://w3id.org/ci#PartOf) (op) **some** [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[ci:hasActivity](https://w3id.org/ci#hasActivity) (op) **exactly** 1 [ci:Activity](https://w3id.org/ci#Activity) (c)<br />[cterm:hasClassification](https://w3id.org/cterm#hasClassification) **some** [cterm:Classification](https://w3id.org/cterm#Classification) (c)<br />[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **exactly** 1 [cterm:Material](https://w3id.org/cterm#Material) (c)<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **max** 1<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfCostComponent](https://w3id.org/cterm#ObjectOfCostComponent) (c)<br />
Sub-classes |[ci:ConstructionComponent](https://w3id.org/ci#ConstructionComponent) (c)<br />[ci:TemporaryComponent](https://w3id.org/ci#TemporaryComponent) (c)<br />[ci:ProductComponent](https://w3id.org/ci#ProductComponent) (c)<br />
In domain of |[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op)<br />[ci:SubComponentOf](https://w3id.org/ci#SubComponentOf) (op)<br />[ci:PartOf](https://w3id.org/ci#PartOf) (op)<br />[ci:hasActivity](https://w3id.org/ci#hasActivity) (op)<br />[ci:code](https://w3id.org/ci#code) (dp)<br />[ci:measurementRules](https://w3id.org/ci#measurementRules) (dp)<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp)<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op)<br />[ci:hasWork](https://w3id.org/ci#hasWork) (op)<br />
In range of |[ci:ActivityOf](https://w3id.org/ci#ActivityOf) (op)<br />[ci:SubComponentOf](https://w3id.org/ci#SubComponentOf) (op)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op)<br />[ci:UnitOf](https://w3id.org/ci#UnitOf) (op)<br />[ci:hasPart](https://w3id.org/ci#hasPart) (op)<br />[ci:WorkOf](https://w3id.org/ci#WorkOf) (op)<br />
### CostItem
Property | Value
--- | ---
IRI | `https://w3id.org/ci#CostItem`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **exactly** 1<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:unit](http://qudt.org/schema/qudt/unit) (c)<br />[ci:unitPrice](https://w3id.org/ci#unitPrice) (dp) **exactly** 1<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[ci:hasPart](https://w3id.org/ci#hasPart) (op) **some** [ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[cterm:hasClassification](https://w3id.org/cterm#hasClassification) **some** [cterm:Classification](https://w3id.org/cterm#Classification) (c)<br />[ci:prefix](https://w3id.org/ci#prefix) (dp) **exactly** 1<br />
In domain of |[ci:hasPart](https://w3id.org/ci#hasPart) (op)<br />[ci:prefix](https://w3id.org/ci#prefix) (dp)<br />[ci:code](https://w3id.org/ci#code) (dp)<br />[ci:unitPrice](https://w3id.org/ci#unitPrice) (dp)<br />
In range of |[ci:PartOf](https://w3id.org/ci#PartOf) (op)<br />
### Product Work
Property | Value
--- | ---
IRI | `https://w3id.org/ci#ProductComponent`
Super-classes |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Restrictions |[ci:hasWork](https://w3id.org/ci#hasWork) (op) **exactly** 1 [ci:WorkOfProductComponent](https://w3id.org/ci#WorkOfProductComponent) (c)<br />
### ProductionResult
Property | Value
--- | ---
IRI | `https://w3id.org/ci#ProductionResult`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ci:hasPart](https://w3id.org/ci#hasPart) (op) **some** [ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
In domain of |[ci:hasPart](https://w3id.org/ci#hasPart) (op)<br />
In range of |[ci:PartOf](https://w3id.org/ci#PartOf) (op)<br />
### Temporary Work
Property | Value
--- | ---
IRI | `https://w3id.org/ci#TemporaryComponent`
Super-classes |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Restrictions |[ci:hasWork](https://w3id.org/ci#hasWork) (op) **exactly** 1 [ci:WorkOfTemporaryComponent](https://w3id.org/ci#WorkOfTemporaryComponent) (c)<br />
### Work
Property | Value
--- | ---
IRI | `https://w3id.org/ci#Work`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **exactly** 1 [cterm:Material](https://w3id.org/cterm#Material) (c)<br />[ci:techSpecs](https://w3id.org/ci#techSpecs) (dp) **max** 1<br />[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **max** 1<br />[cterm:hasPhysicalParameter](https://w3id.org/cterm#hasPhysicalParameter) **max** 10 [cterm:PhysicalParameter](https://w3id.org/cterm#PhysicalParameter) (c)<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[ci:law](https://w3id.org/ci#law) (dp) **max** 10<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **exactly** 1 [cterm:FamilyOfWork](https://w3id.org/cterm#FamilyOfWork) (c)<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[cterm:hasOtherStandard](https://w3id.org/cterm#hasOtherStandard) **max** 5 [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />[cterm:hasPerformanceParameter](https://w3id.org/cterm#hasPerformanceParameter) **max** 10 [cterm:PerformanceParameter](https://w3id.org/cterm#PerformanceParameter) (c)<br />[ci:cam](https://w3id.org/ci#cam) (dp) **max** 1<br />[cterm:hasDimensionParameter](https://w3id.org/cterm#hasDimensionParameter) **max** 10 [cterm:DimensionParameter](https://w3id.org/cterm#DimensionParameter) (c)<br />
Sub-classes |[ci:WorkOfConstructionComponent](https://w3id.org/ci#WorkOfConstructionComponent) (c)<br />[ci:WorkOfProductComponent](https://w3id.org/ci#WorkOfProductComponent) (c)<br />[ci:WorkOfTemporaryComponent](https://w3id.org/ci#WorkOfTemporaryComponent) (c)<br />
In domain of |[ci:excluded](https://w3id.org/ci#excluded) (dp)<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op)<br />[ci:law](https://w3id.org/ci#law) (dp)<br />[ci:WorkOf](https://w3id.org/ci#WorkOf) (op)<br />[ci:cam](https://w3id.org/ci#cam) (dp)<br />[ci:techSpecs](https://w3id.org/ci#techSpecs) (dp)<br />[ci:keywords](https://w3id.org/ci#keywords) (dp)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op)<br />[ci:code](https://w3id.org/ci#code) (dp)<br />[ci:included](https://w3id.org/ci#included) (dp)<br />
In range of |[ci:hasWork](https://w3id.org/ci#hasWork) (op)<br />[ci:UnitOf](https://w3id.org/ci#UnitOf) (op)<br />[ci:SubComponentOf](https://w3id.org/ci#SubComponentOf) (op)<br />
### WorkOfConstructionWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#WorkOfConstructionComponent`
Super-classes |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Restrictions |[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **max** 1 [cterm:FunctionOfWorkOfConstructionWork](https://w3id.org/cterm#FunctionOfWorkOfConstructionWork) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **max** 5 [cterm:UseOfWorkOfConstructionWork](https://w3id.org/cterm#UseOfWorkOfConstructionWork) (c)<br />[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **max** 5 [cterm:FinishingOfWorkOfConstructionWork](https://w3id.org/cterm#FinishingOfWorkOfConstructionWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:ProductComponent](https://w3id.org/ci#ProductComponent) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **max** 1 [cterm:TypeOfWorkOfConstructionWork](https://w3id.org/cterm#TypeOfWorkOfConstructionWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:ConstructionComponent](https://w3id.org/ci#ConstructionComponent) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **max** 5 [cterm:AspectOfWorkOfConstructionWork](https://w3id.org/cterm#AspectOfWorkOfConstructionWork) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfWorkOfConstructionWork](https://w3id.org/cterm#CategoryOfWorkOfConstructionWork) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfWorkOfConstructionWork](https://w3id.org/cterm#ObjectOfWorkOfConstructionWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />
### WorkOfProductWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#WorkOfProductComponent`
Super-classes |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Restrictions |[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **max** 5 [cterm:AspectOfWorkOfProductWork](https://w3id.org/cterm#AspectOfWorkOfProductWork) (c)<br />[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **max** 5 [cterm:FinishingOfWorkOfProductWork](https://w3id.org/cterm#FinishingOfWorkOfProductWork) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfWorkOfProductWork](https://w3id.org/cterm#ObjectOfWorkOfProductWork) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **max** 1 [cterm:TypeOfWorkOfProductWork](https://w3id.org/cterm#TypeOfWorkOfProductWork) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfWorkOfProductWork](https://w3id.org/cterm#CategoryOfWorkOfProductWork) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **max** 5 [cterm:UseOfWorkOfProductWork](https://w3id.org/cterm#UseOfWorkOfProductWork) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **max** 1 [cterm:FunctionOfWorkOfProductWork](https://w3id.org/cterm#FunctionOfWorkOfProductWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />
### WorkOfTemporaryWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#WorkOfTemporaryComponent`
Super-classes |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Restrictions |[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **max** 1 [cterm:FunctionOfWorkOfTemporaryWork](https://w3id.org/cterm#FunctionOfWorkOfTemporaryWork) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfWorkOfTemporaryWork](https://w3id.org/cterm#ObjectOfWorkOfTemporaryWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:ProductComponent](https://w3id.org/ci#ProductComponent) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **exactly** 1 [cterm:TypeOfWorkOfTemporaryWork](https://w3id.org/cterm#TypeOfWorkOfTemporaryWork) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **max** 5 [cterm:AspectOfWorkOfTemporaryWork](https://w3id.org/cterm#AspectOfWorkOfTemporaryWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **max** 5 [cterm:FinishingOfWorkOfTemporaryWork](https://w3id.org/cterm#FinishingOfWorkOfTemporaryWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfWorkOfTemporaryWork](https://w3id.org/cterm#CategoryOfWorkOfTemporaryWork) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **max** 5 [cterm:UseOfWorkOfTemporaryWork](https://w3id.org/cterm#UseOfWorkOfTemporaryWork) (c)<br />

## Object Properties
[Activity of](#Activityof),
[PartOf](#PartOf),
[SubComponentOf](#SubComponentOf),
[UnitOf](#UnitOf),
[WorkOf](#WorkOf),
[hasActivity](#hasActivity),
[hasPart](#hasPart),
[hasSubComponent](#hasSubComponent),
[hasUnit](#hasUnit),
[hasWork](#hasWork),
[](Activityof)
### Activity of
Property | Value
--- | ---
IRI | `https://w3id.org/ci#ActivityOf`
Domain(s) |[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
[](PartOf)
### PartOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#PartOf`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[ci:ProductionResult](https://w3id.org/ci#ProductionResult) (c)<br />[ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />
[](SubComponentOf)
### SubComponentOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#SubComponentOf`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />
[](UnitOf)
### UnitOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#UnitOf`
Domain(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
[](WorkOf)
### WorkOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#WorkOf`
Domain(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
[](hasActivity)
### hasActivity
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasActivity`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
[](hasPart)
### hasPart
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasPart`
Domain(s) |[ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[ci:ProductionResult](https://w3id.org/ci#ProductionResult) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
[](hasSubComponent)
### hasSubComponent
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasSubComponent`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
[](hasUnit)
### hasUnit
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasUnit`
Domain(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](hasWork)
### hasWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasWork`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />

## Datatype Properties
[environmental and ecological requirements defined by the Italian Ministry of Environment](#environmentalandecologicalrequirementsdefinedbytheItalianMinistryofEnvironment),
[code](#code),
[descriptionDetail](#descriptionDetail),
[descriptionGeneral](#descriptionGeneral),
[excluded](#excluded),
[included](#included),
[keywords](#keywords),
[law](#law),
[measurementRules](#measurementRules),
[prefisso](#prefisso),
[quantityUnitOfMeasure](#quantityUnitOfMeasure),
[tech specs](#techspecs),
[unit price](#unitprice),
[](environmentalandecologicalrequirementsdefinedbytheItalianMinistryofEnvironment)
### environmental and ecological requirements defined by the Italian Ministry of Environment
Property | Value
--- | ---
IRI | `https://w3id.org/ci#cam`
Domain(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](code)
### code
Property | Value
--- | ---
IRI | `https://w3id.org/ci#code`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />[ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](descriptionDetail)
### descriptionDetail
Property | Value
--- | ---
IRI | `https://w3id.org/ci#descriptionDetail`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](descriptionGeneral)
### descriptionGeneral
Property | Value
--- | ---
IRI | `https://w3id.org/ci#descriptionGeneral`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](excluded)
### excluded
Property | Value
--- | ---
IRI | `https://w3id.org/ci#excluded`
Domain(s) |[ci:Activity](https://w3id.org/ci#Activity) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](included)
### included
Property | Value
--- | ---
IRI | `https://w3id.org/ci#included`
Domain(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](keywords)
### keywords
Property | Value
--- | ---
IRI | `https://w3id.org/ci#keywords`
Domain(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](law)
### law
Property | Value
--- | ---
IRI | `https://w3id.org/ci#law`
Domain(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](measurementRules)
### measurementRules
Property | Value
--- | ---
IRI | `https://w3id.org/ci#measurementRules`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](prefisso)
### prefisso
Property | Value
--- | ---
IRI | `https://w3id.org/ci#prefix`
Domain(s) |[ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](quantityUnitOfMeasure)
### quantityUnitOfMeasure
Property | Value
--- | ---
IRI | `https://w3id.org/ci#quantityUnitOfMeasure`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](techspecs)
### tech specs
Property | Value
--- | ---
IRI | `https://w3id.org/ci#techSpecs`
Domain(s) |[ci:Activity](https://w3id.org/ci#Activity) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](unitprice)
### unit price
Property | Value
--- | ---
IRI | `https://w3id.org/ci#unitPrice`
Domain(s) |[ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />

## Named Individuals
## Namespaces
* **ci**
  * `https://w3id.org/ci#`
* **cr**
  * `https://w3id.org/cr#`
* **cterm**
  * `https://w3id.org/cterm#`
* **dc**
  * `http://purl.org/dc/terms/`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **qudt**
  * `http://qudt.org/schema/qudt/`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **vs**
  * `http://www.w3.org/2003/06/sw-vocab-status/ns#`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni