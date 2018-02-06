class Shapes:
    def __init__(self, name, length, breadth):
        self.length = length
        self.breadth = breadth
    @property
    def area(self):
        return self.length*self.breadth

    def perimeter(self):
        print " the perimeter is :",2*(self.length+self.breadth)


s1 = Shapes('triangle', 2, 4)

class Triangle(Shapes):
    def __init__(self, name, length, breadth, height):
        Shapes.__init__(self, name, length, breadth)
        self.height = height

    def area_triangle(self):
        return 'the area is :', ((self.breadth*self.height)/2)

    def perimeter_triangle(self):
        return 'the perimeter of triangle:',(self.length+self.breadth+self.height)


t1=Triangle("trinagle",2,4,5)
#print t1.area_triangle()
#print t1.perimeter_triangle()

class Equitriangle(Triangle):

    def __init__(self, name, length, breadth, height, angle):
        Triangle.__init__(self, name, length, breadth, height)
        self.angle = angle

    def area_equi(self):
        if self.length==self.breadth:
            return ((self.length*self.height)/2)
        else:
           return "not an equilateral triangle"

#e1 = Equitriangle("equi",5,4,5,60)
#print e1.area_equi()

class Rectangless(Shapes):
    length=4
    breadth=6
    def __init__(self, name, length, breadth, height):
        Shapes.__init__(self, name, length, breadth)
        self.height = height

    def area_rect(self):
        print self.length+self.breadth

r1=Rectangle("rect",3,4,5)
print r1.area()
