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
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum, Computing in Engineering](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
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
  * 2025-04-07
* **Version Information**
  * 0.2
* **Imports**
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
Restrictions |[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfActivity](https://w3id.org/cterm#ObjectOfActivity) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **some** [cterm:UseOfActivity](https://w3id.org/cterm#UseOfActivity) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **some** [cterm:FunctionOfActivity](https://w3id.org/cterm#FunctionOfActivity) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:LabourResource](https://w3id.org/cr#LabourResource) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:TemporaryComponent](https://w3id.org/ci#TemporaryComponent) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfActivity](https://w3id.org/cterm#CategoryOfActivity) (c)<br />[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **max** 1<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **only** [cterm:FamilyOfActivity](https://w3id.org/cterm#FamilyOfActivity) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **only** [cterm:TypeOfActivity](https://w3id.org/cterm#TypeOfActivity) (c)<br />[ci:techSpecs](https://w3id.org/ci#techSpecs) (dp) **max** 1<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />
In domain of |[ci:activityOf](https://w3id.org/ci#activityOf) (op)<br />
In range of |[ci:hasActivity](https://w3id.org/ci#hasActivity) (op)<br />
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
Restrictions |[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfCostComponent](https://w3id.org/cterm#ObjectOfCostComponent) (c)<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **max** 1<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfCostComponent](https://w3id.org/cterm#CategoryOfCostComponent) (c)<br />[ci:partOf](https://w3id.org/ci#partOf) (op) **some** [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[ci:hasActivity](https://w3id.org/ci#hasActivity) (op) **exactly** 1 [ci:Activity](https://w3id.org/ci#Activity) (c)<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **only** [cterm:FamilyOfCostComponent](https://w3id.org/cterm#FamilyOfCostComponent) (c)<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[cterm:hasClassification](https://w3id.org/cterm#hasClassification) **some** [cterm:Classification](https://w3id.org/cterm#Classification) (c)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **only** [cterm:Material](https://w3id.org/cterm#Material) (c)<br />
Sub-classes |[ci:ConstructionComponent](https://w3id.org/ci#ConstructionComponent) (c)<br />[ci:TemporaryComponent](https://w3id.org/ci#TemporaryComponent) (c)<br />[ci:ProductComponent](https://w3id.org/ci#ProductComponent) (c)<br />
In domain of |[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp)<br />[ci:hasActivity](https://w3id.org/ci#hasActivity) (op)<br />[ci:measurementRules](https://w3id.org/ci#measurementRules) (dp)<br />[ci:partOf](https://w3id.org/ci#partOf) (op)<br />[ci:hasWork](https://w3id.org/ci#hasWork) (op)<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp)<br />
In range of |[ci:activityOf](https://w3id.org/ci#activityOf) (op)<br />[ci:workOf](https://w3id.org/ci#workOf) (op)<br />[ci:hasPart](https://w3id.org/ci#hasPart) (op)<br />
### CostItem
Property | Value
--- | ---
IRI | `https://w3id.org/ci#CostItem`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **exactly** 1<br />[ci:prefix](https://w3id.org/ci#prefix) (dp) **exactly** 1<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:unit](http://qudt.org/schema/qudt/unit) (c)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[ci:unitPrice](https://w3id.org/ci#unitPrice) (dp) **exactly** 1<br />[cterm:hasClassification](https://w3id.org/cterm#hasClassification) **some** [cterm:Classification](https://w3id.org/cterm#Classification) (c)<br />[ci:hasPart](https://w3id.org/ci#hasPart) (op) **some** [ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
In domain of |[ci:unitPrice](https://w3id.org/ci#unitPrice) (dp)<br />[ci:prefix](https://w3id.org/ci#prefix) (dp)<br />
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
Restrictions |[ci:techSpecs](https://w3id.org/ci#techSpecs) (dp) **max** 1<br />[cterm:hasOtherStandard](https://w3id.org/cterm#hasOtherStandard) **some** [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[ci:quantityUnitOfMeasure](https://w3id.org/ci#quantityUnitOfMeasure) (dp) **exactly** 1<br />[ci:descriptionGeneral](https://w3id.org/ci#descriptionGeneral) (dp) **exactly** 1<br />[ci:code](https://w3id.org/ci#code) (dp) **exactly** 1<br />[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **only** [cterm:Material](https://w3id.org/cterm#Material) (c)<br />[ci:law](https://w3id.org/ci#law) (dp) **some** [xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />[ci:descriptionDetail](https://w3id.org/ci#descriptionDetail) (dp) **max** 1<br />[cterm:hasDimensionParameter](https://w3id.org/cterm#hasDimensionParameter) **some** [cterm:DimensionParameter](https://w3id.org/cterm#DimensionParameter) (c)<br />[ci:cam](https://w3id.org/ci#cam) (dp) **max** 1<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **only** [cterm:FamilyOfWork](https://w3id.org/cterm#FamilyOfWork) (c)<br />[cterm:hasPerformanceParameter](https://w3id.org/cterm#hasPerformanceParameter) **some** [cterm:PerformanceParameter](https://w3id.org/cterm#PerformanceParameter) (c)<br />[cterm:hasPhysicalParameter](https://w3id.org/cterm#hasPhysicalParameter) **some** [cterm:PhysicalParameter](https://w3id.org/cterm#PhysicalParameter) (c)<br />[ci:hasUnit](https://w3id.org/ci#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
Sub-classes |[ci:WorkOfTemporaryComponent](https://w3id.org/ci#WorkOfTemporaryComponent) (c)<br />[ci:WorkOfConstructionComponent](https://w3id.org/ci#WorkOfConstructionComponent) (c)<br />[ci:WorkOfProductComponent](https://w3id.org/ci#WorkOfProductComponent) (c)<br />
In domain of |[ci:cam](https://w3id.org/ci#cam) (dp)<br />[ci:law](https://w3id.org/ci#law) (dp)<br />[ci:workOf](https://w3id.org/ci#workOf) (op)<br />
In range of |[ci:hasWork](https://w3id.org/ci#hasWork) (op)<br />
### WorkOfConstructionWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#WorkOfConstructionComponent`
Super-classes |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Restrictions |[cterm:hasUse](https://w3id.org/cterm#hasUse) **some** [cterm:UseOfWorkOfConstructionWork](https://w3id.org/cterm#UseOfWorkOfConstructionWork) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfWorkOfConstructionWork](https://w3id.org/cterm#CategoryOfWorkOfConstructionWork) (c)<br />[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **some** [cterm:FinishingOfWorkOfConstructionWork](https://w3id.org/cterm#FinishingOfWorkOfConstructionWork) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **only** [cterm:TypeOfWorkOfConstructionWork](https://w3id.org/cterm#TypeOfWorkOfConstructionWork) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfWorkOfConstructionWork](https://w3id.org/cterm#ObjectOfWorkOfConstructionWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:ProductComponent](https://w3id.org/ci#ProductComponent) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **some** [cterm:AspectOfWorkOfConstructionWork](https://w3id.org/cterm#AspectOfWorkOfConstructionWork) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **some** [cterm:FunctionOfWorkOfConstructionWork](https://w3id.org/cterm#FunctionOfWorkOfConstructionWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:ConstructionComponent](https://w3id.org/ci#ConstructionComponent) (c)<br />
### WorkOfProductWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#WorkOfProductComponent`
Super-classes |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Restrictions |[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **some** [cterm:FinishingOfWorkOfProductWork](https://w3id.org/cterm#FinishingOfWorkOfProductWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfWorkOfProductWork](https://w3id.org/cterm#CategoryOfWorkOfProductWork) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **some** [cterm:UseOfWorkOfProductWork](https://w3id.org/cterm#UseOfWorkOfProductWork) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfWorkOfProductWork](https://w3id.org/cterm#ObjectOfWorkOfProductWork) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **only** [cterm:TypeOfWorkOfProductWork](https://w3id.org/cterm#TypeOfWorkOfProductWork) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **some** [cterm:FunctionOfWorkOfProductWork](https://w3id.org/cterm#FunctionOfWorkOfProductWork) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **some** [cterm:AspectOfWorkOfProductWork](https://w3id.org/cterm#AspectOfWorkOfProductWork) (c)<br />
### WorkOfTemporaryWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#WorkOfTemporaryComponent`
Super-classes |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Restrictions |[cterm:hasUse](https://w3id.org/cterm#hasUse) **some** [cterm:UseOfWorkOfTemporaryWork](https://w3id.org/cterm#UseOfWorkOfTemporaryWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [ci:ProductComponent](https://w3id.org/ci#ProductComponent) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfWorkOfTemporaryWork](https://w3id.org/cterm#ObjectOfWorkOfTemporaryWork) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfWorkOfTemporaryWork](https://w3id.org/cterm#CategoryOfWorkOfTemporaryWork) (c)<br />[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **some** [cterm:FinishingOfWorkOfTemporaryWork](https://w3id.org/cterm#FinishingOfWorkOfTemporaryWork) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **some** [cterm:FunctionOfWorkOfTemporaryWork](https://w3id.org/cterm#FunctionOfWorkOfTemporaryWork) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **some** [cterm:AspectOfWorkOfTemporaryWork](https://w3id.org/cterm#AspectOfWorkOfTemporaryWork) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />[ci:hasSubComponent](https://w3id.org/ci#hasSubComponent) (op) **some** [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **only** [cterm:TypeOfWorkOfTemporaryWork](https://w3id.org/cterm#TypeOfWorkOfTemporaryWork) (c)<br />

## Object Properties
[activity of](#activityof),
[hasActivity](#hasActivity),
[hasPart](#hasPart),
[hasSubComponent](#hasSubComponent),
[hasUnit](#hasUnit),
[hasWork](#hasWork),
[partOf](#partOf),
[subComponentOf](#subComponentOf),
[unitOf](#unitOf),
[workOf](#workOf),
[](activityof)
### activity of
Property | Value
--- | ---
IRI | `https://w3id.org/ci#activityOf`
Domain(s) |[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
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
Domain(s) |([ci:CostItem](https://w3id.org/ci#CostItem) (c) or [ci:ProductionResult](https://w3id.org/ci#ProductionResult) (c))<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
[](hasSubComponent)
### hasSubComponent
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasSubComponent`
Domain(s) |([ci:CostComponent](https://w3id.org/ci#CostComponent) (c) or [ci:Work](https://w3id.org/ci#Work) (c) or [ci:Activity](https://w3id.org/ci#Activity) (c))<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
[](hasUnit)
### hasUnit
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasUnit`
Domain(s) |([ci:CostComponent](https://w3id.org/ci#CostComponent) (c) or [ci:Work](https://w3id.org/ci#Work) (c) or [ci:Activity](https://w3id.org/ci#Activity) (c))<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](hasWork)
### hasWork
Property | Value
--- | ---
IRI | `https://w3id.org/ci#hasWork`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />
[](partOf)
### partOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#partOf`
Domain(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />
Range(s) |[ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[ci:ProductionResult](https://w3id.org/ci#ProductionResult) (c)<br />
[](subComponentOf)
### subComponentOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#subComponentOf`
Domain(s) |([ci:CostComponent](https://w3id.org/ci#CostComponent) (c) or [cr:Resource](https://w3id.org/cr#Resource) (c))<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
[](unitOf)
### unitOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#unitOf`
Domain(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />[ci:Work](https://w3id.org/ci#Work) (c)<br />[ci:Activity](https://w3id.org/ci#Activity) (c)<br />
[](workOf)
### workOf
Property | Value
--- | ---
IRI | `https://w3id.org/ci#workOf`
Domain(s) |[ci:Work](https://w3id.org/ci#Work) (c)<br />
Range(s) |[ci:CostComponent](https://w3id.org/ci#CostComponent) (c)<br />

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
Domain(s) |([ci:CostItem](https://w3id.org/ci#CostItem) (c) or [ci:CostComponent](https://w3id.org/ci#CostComponent) (c) or [ci:Work](https://w3id.org/ci#Work) (c) or [ci:Activity](https://w3id.org/ci#Activity) (c))<br />
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
Domain(s) |([ci:Work](https://w3id.org/ci#Work) (c) or [ci:Activity](https://w3id.org/ci#Activity) (c))<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](included)
### included
Property | Value
--- | ---
IRI | `https://w3id.org/ci#included`
Domain(s) |([ci:Work](https://w3id.org/ci#Work) (c) or [ci:Activity](https://w3id.org/ci#Activity) (c))<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](keywords)
### keywords
Property | Value
--- | ---
IRI | `https://w3id.org/ci#keywords`
Domain(s) |([ci:Work](https://w3id.org/ci#Work) (c) or [ci:Activity](https://w3id.org/ci#Activity) (c))<br />
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
Domain(s) |([ci:Work](https://w3id.org/ci#Work) (c) or [ci:Activity](https://w3id.org/ci#Activity) (c))<br />
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