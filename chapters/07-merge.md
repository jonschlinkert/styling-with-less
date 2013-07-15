### Chapter 7: `!merge`: Property-level Inheritance

(I'm not sure that "property-level inheritance" is an accurate description for !merge, suggestions or pull-requests are welcome.)

In this chapter we will construct a component that makes heavy use of transforms, such as a navigation slider or carousel. Some of the styles we create in this chapter will also be shuffled into the mixin library we started in [Chapter 5](#chapter-5).

`!merge` works at the property-level in a similar way to how mixins work at the selector level, except that `!merge` enables aggregating values from multiple "source" properties into single "destination" property, which is most advantageous with properties such as background and transform.

**Topics discussed**:

* How `!merge` works
* Merging box shadows
* Merging background gradients
* Merging transforms