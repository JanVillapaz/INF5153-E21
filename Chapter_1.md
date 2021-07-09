# 1.3.1 Classes

In many object-oriented approaches, it is possible to define classes that describe the attributes and the behavior of a set of objects (the instances of a class) abstractly and thus group common features of objects. For example, people have a name, an address, and a social security number. Courses have a unique identifier, a title, and a description. Lecture halls have a name as well as a location, etc. A class also defines a set of permitted operations that can be applied to the instaces of the class. FOr example, you can reserve a lecture hall for a certain date, a student can register for an exam, etc. In this way, classes describe the behavior of objets. 

1.3.2 Objects

The instances of a class are referred to as its objects. For example, lh1, the Lecture Hall 1 of the Vienna University of Technology, is a concrete instance of the class LectureHall. In particular, an object is distinguished by the fact that it has its own identity, that is, different instances of a class can be uniquely identified. For example, the beamer in Lecture Hall 1 is a different object to the beamer in Lecture Hall 2, even if the devices are of the same type. Here we refer to identical devices but not the same device. The situation for concrete values of data types is different; the number 1, which is a concrete value of data type Integer, does not have a distinguishable identity.

An object always has a certain state. A state is expressed by the values of its attributes. For example, a lecture hall can have the state occupied for free. An object also displays behavior. The behavior of an object is described by the set of its operations. Operations are triggered by sending a message. 

1.3.3 Encapsulation

Encapsulation is the protection against unauthorized access to the internal state of an object via a uniquely defined interface. Different levels of visibility of the interfaces help to define different access authorizations. Java, for example, has the explicit visibility markers `public`, `private`, and `protected`, which respectively permit access for all, only within the object, and only for members of the same class, its subclasses, and of the same package.

1.3.4 Messages
