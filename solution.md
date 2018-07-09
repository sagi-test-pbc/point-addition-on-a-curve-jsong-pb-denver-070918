
# Point Addition on a Curve


```python
# Example where x1 != x2

from ecc import FieldElement, Point

prime = 137
a = FieldElement(0, prime)
b = FieldElement(7, prime)
p1 = Point(FieldElement(73, prime), FieldElement(128, prime), a, b)
p2 = Point(FieldElement(46, prime), FieldElement(22, prime), a, b)

print(p1+p2)
```

### Try it

#### Find the following point additions on the curve  \\( y^2 = x^3 + 7: F_{223} \\)
```
(192,105) + (17,56), (47,71) + (117,141), (143,98) + (76,66)
```


```python
from ecc import FieldElement, Point

prime = 223
a = FieldElement(0, prime)
b = FieldElement(7, prime)

additions = ((192, 105, 17, 56), (47, 71, 117, 141), (143, 98, 76, 66))

# iterate over the additions to be done
for x1_raw, y1_raw, x2_raw, y2_raw in additions:
    # Initialize points this way:
    # x1 = FieldElement(x1_raw, prime)
    # y1 = FieldElement(y1_raw, prime)
    # p1 = Point(x1, y1, a, b)
    # x2 = FieldElement(x2_raw, prime)
    # y2 = FieldElement(y2_raw, prime)
    # p2 = Point(x2, y2, a, b)
    x1 = FieldElement(x1_raw, prime)
    y1 = FieldElement(y1_raw, prime)
    p1 = Point(x1, y1, a, b)
    x2 = FieldElement(x2_raw, prime)
    y2 = FieldElement(y2_raw, prime)
    p2 = Point(x2, y2, a, b)
    print('{} + {} = {}'.format(p1, p2, p1+p2))
```
