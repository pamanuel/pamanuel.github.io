---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
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
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

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
