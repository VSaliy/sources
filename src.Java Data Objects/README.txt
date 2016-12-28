Java Data Objects

Right at the moment when the authors were completing the book,
a change was made to the reference enhancer syntax for JDO 1.0.1.
The book is based on JDO 1.0.1. Specifically, a new flag was
introduced and the approached used in JDO for naming and looking
up the metadata was changed.

Unfortuately, two things have occurred:
1. The authors did not get the reference enhancer syntax
updated correctly in all the places in the book.
2. Sun has not yet released JDO 1.0.1, only JDO 1.0 is
currently available. The authors had expected Sun to release
JDO 1.0.1 about the same time as the book's release.
Unfortunately, that did not happen.
The JDO 1.0.1 reference enhancer syntax will not work with
the JDO 1.0 reference enhancer implementation.

The description below specifies how to enhance JDO classes
with either the JDO 1.0 or 1.0.1 reference enhancer.

David Jordan
Object Identity, Inc.
www.objectidentity.com

==================================

During the writing of Java Data Objects, JDO 1.0.1 was being prepared
for public release, and we expected that the release of the book and the
specification would be concurrent. However, the release of the
specification, including the reference implementation, was delayed. In
order to run the examples in the book using either JDO 1.0 or JDO 1.0.1,
please use this information.

There are two examples of using the enhancer in the book. The first is
in Chapter 1, p. 11, Example 1-5.

To use this with the JDO 1.0.1, the metadata file is
classes/com/mediamania/prototype/package.jdo and the command line is:

com.sun.jdori.enhancer.Main -d enhanced -s classes \
classes/com/mediamania/prototype/Movie.class \
classes/com/mediamania/prototype/Actor.class \
classes/com/mediamania/prototype/Role.class

To use this example with JDO 1.0 enhancer, the metadata file is
classes/com/mediamania/prototype.jdo and the command line is:

com.sun.jdori.enhancer.Main -d enhanced \
classes/com/mediamania/prototype.jdo \
classes/com/mediamania/prototype/Movie.class \
classes/com/mediamania/prototype/Actor.class \
classes/com/mediamania/prototype/Role.class

The second example is in Chapter 6, p. 96.

To use this example with JDO 1.0.1, the metadata file is
classes/com/mediamania/package.jdo and the command line is:

java com.sun.jdori.enhancer.Main -d enhanced -s classes \
classes/com/mediamania/content/Studio.class \
classes/com/mediamania/content/MediaContent.class \
classes/com/mediamania/content/Movie.class \
classes/com/mediamania/content/Game.class \
classes/com/mediamania/content/Role.class \
classes/com/mediamania/content/MediaPerson.class \
classes/com/mediamania/store/MediaItem.class \
classes/com/mediamania/store/RentalItem.class \
classes/com/mediamania/store/RentalCode.class \
classes/com/mediamania/store/Customer.class \
classes/com/mediamania/store/Address.class \
classes/com/mediamania/store/Transaction.class \
classes/com/mediamania/store/Purchase.class \
classes/com/mediamania/store/Rental.class

To use this example with JDO 1.0, the metadata file is
classes/com/mediamania.jdo and the command line is:

java com.sun.jdori.enhancer.Main -d enhanced \
classes/com/mediamania.jdo \
classes/com/mediamania/content/Studio.class \
classes/com/mediamania/content/MediaContent.class \
classes/com/mediamania/content/Movie.class \
classes/com/mediamania/content/Game.class \
classes/com/mediamania/content/Role.class \
classes/com/mediamania/content/MediaPerson.class \
classes/com/mediamania/store/MediaItem.class \
classes/com/mediamania/store/RentalItem.class \
classes/com/mediamania/store/RentalCode.class \
classes/com/mediamania/store/Customer.class \
classes/com/mediamania/store/Address.class \
classes/com/mediamania/store/Transaction.class \
classes/com/mediamania/store/Purchase.class \
classes/com/mediamania/store/Rental.class