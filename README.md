# inhert-Exa
public class Main {
    public static void main(String[] args) {
        Shape s = new Shape("green", true);
        System.out.println("" + s.getColor());
        System.out.println("" + s.toString());
        Circle c=new Circle(30);
        System.out.println(""+c.getPremeter());
        Circle c1=new Circle(100);
        System.out.println(""+c1.getArea());

        Rectangle r1=new Rectangle(55,77);
        System.out.println(""+r1.getLenght());
        System.out.println(""+r1.getWidth());
        Rectangle r2=new Rectangle(66,100,"white",true);
        System.out.println(""+r2.getArea());
        System.out.println(""+r2.getPremeter());

        Square s1=new Square(200,100,100,"white",true);
        Square s2=new Square(22);
//        s2.setSide(44);
       System.out.println(""+s1.getArea());
       s1.setSide_w(20);
        System.out.println(""+s1.getSide_w());
     System.out.printf(""+s1.toString());

    }
}
<!--  -->
public class Shape {
    private String color;
    private boolean filled;
    public Shape(){}

    public Shape(String color, boolean filled) {
        this.color = color;
        this.filled = filled;
    }

    public String getColor() {
        return color;
    }

    public void setColor(String color) {
        this.color = color;
    }

    public boolean isFilled() {
        return filled;
    }
    public void setFilled(boolean filled) {
        this.filled = filled;
    }
}
<!--Rectangle classs  -->
public class Rectangle extends Shape {
    private double width;
    private double lenght;

    public Rectangle() {
//        width=1.0;
//        lenght=1.0;
        System.out.printf("the intilize value To lenthg and width is "+width+lenght);
    }
    public Rectangle(double width1, double lenght1) {
        this.width = width1;
        this.lenght = lenght1;
    }
    public Rectangle(double width, double lenght,String color,boolean filled) {
        this.width = width;
        this.lenght = lenght;

    }
    public double getWidth() {
        return width;
    }

    public void setWidth(double width) {
        this.width = width;
    }

    public double getLenght() {
        return lenght;
    }

    public void setLenght(double lenght) {
        this.lenght = lenght;
    }
    public double getArea() {
//      raduies=raduies;
        return lenght*width;
    }

    public double getPremeter() {
        return 2*lenght*width;}

}
<!-- Circle -->
public class Circle extends Shape{
    double raduies;
    //ميثود ماهي بارميتر
    //double area;
   // int premeter;

     public Circle(){
       raduies=1;}
    public Circle(double raduies) {
        this.raduies = raduies;
    }
    public Circle(String color, boolean filled, double raduies) {
        super(color, filled);
        this.raduies = raduies;
    }

    public double getRaduies() {
        return raduies;
    }

    public void setRaduies(double raduies) {
        this.raduies = raduies;
    }

    public double getArea() {
        return raduies*3.14;
    }

    public double getPremeter() {
        return 2*raduies*3.14/2;}
    }
<!--Squer  -->
public class Square extends Rectangle {
    //مافيه اتربيوت يعني اسوي   كونستركتر يلبي الاحتياج
    // ارث الميثود الباقيه من الركتانقل الودث هو نفسه السايد يعني باخذ الودث وارسله

//    ماطلع فبجرب اتربيوت
    private double side_w;

    public double getSide_w() {
        side_w=side_w*4;
        return side_w;
    }public void setSide_w(double side_w) {
        this.side_w = side_w;
    }

    public Square(){}
   public Square(double side) {
        super(side,side);
    }
//    }

    public Square(double side,double width1, double lenght1, String color, boolean filled) {
        super(width1, lenght1, color, filled);

    }
    //اللي هي المفروض مساحة المربع الطول بالعرض
    @Override
    public double getArea() {

        return getArea();
    }
    public String toString(){

       return "The lenghth"+super.getLenght()+"The color"+super.getColor()+"filled"+super.isFilled();
    }
}


