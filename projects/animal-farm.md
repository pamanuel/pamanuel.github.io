---
layout: project
type: project
image: img/animal_farm_full.jpeg
title: "Animal Farm"
date: 2022
published: true
labels:
  - Object Oriented Programming
  - C
  - C++
summary: "Animal Farm is an abundance of small class labs where students were tasked with created a database. Each lab implemented a new feature that taught a different aspect of object-oriented programming."
---

<div class="text-center p-4">
  <img width="200px" src="../img/animal_farm_full.jpeg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>
The Animal Farm labs were given int the EE205 Object-Oriented Programming course given at the University of Hawaii at Manoa, taught by Professor Mark Nelson. The intensions of the lab is to create a database where with each lab we are introduced and asked to implement new aspects of Object Oriented Programming. Initially it started off with storing our objects and it's properties in an array, then structs, then evidently linked lists. When our objects were stored in linked list we were tasked with adding classes. Evidently, our data base was structured so that our database

Here is some code that comes from the header file of my Animal Class where you will see implemtnations of  getters and setters, constructors, inheritence, etc:

```cpp
class Animal: public Node{
public:
    static const std::string KINGDOM_NAME;
private:
    std::string species;
    std::string classification;
    Gender gender = Gender::UNKNOWN_GENDER;
    Weight weight;
public:///constructors///
    Animal(const Weight::t_weight newMaxWeight,
           const std::string &newClassification,
           const std::string &newSpecies);

    Animal(const Gender newGender,
           const Weight::t_weight newWeight,
           const Weight::t_weight newMaxWeight,
           const std::string &newClassification,
           const std::string &newSpecies);
public:///getters and setters///
    std::string getKingdom() const noexcept;
    std::string getClassification() const noexcept;
    std::string getSpecies() const noexcept;
    Gender getGender() const noexcept;
    Weight::t_weight getWeight()const noexcept;
    void setWeight(const Weight::t_weight newWeight);
public:///public methods///
    virtual std::string speak()const noexcept=0;
    void dump() const noexcept override;
    bool validate() const noexcept override;
    ////static public methods///
    static bool validateClassification(const std::string &checkClassification) noexcept;
    static bool validateSpecies(const std::string &checkSpecies) noexcept;
protected:///protected method///
    void setGender(const Gender newGender);
};
```
