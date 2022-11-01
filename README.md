# 4.3

import java.text.NumberFormat;


public class Sphere {
    
    private double diameter1;
    
    public Sphere (double diameter)
    {
        diameter1 = diameter;
    }
    
    public double getDiameter() { return diameter1; }
    public void setDiameter( int diameter){diameter1 = diameter; }
    
    public double getVolume()
    {
        double v = 0;
         
        v = (4.00 / 3) * Math.PI * Math.pow(getDiameter(), 3);
        return v;
    }
    public double getArea()
    {
        double area = 0;
        
        area = 4 * Math.PI * Math.pow(getDiameter(), 2);
        return area;
    }
    
    public String toString()
    {
        NumberFormat fmt = NumberFormat.getNumberInstance();
        return fmt.format(getDiameter());
    }
}

////////////////////////////////////

import java.util.Scanner;
import java.text.DecimalFormat;

public class MultiSphere {

    public static void main(String[] args){
          double r = 0;
          DecimalFormat fmt = new DecimalFormat();
          
          Scanner scan = new Scanner(System.in);
          System.out.println("Enter diameter");
          r = scan.nextDouble();
          
          scan.close();
          
          Sphere sphere = new Sphere(r);
          
          System.out.println(sphere);
          System.out.println(fmt.format(sphere.getVolume()));
          System.out.println(fmt.format(sphere.getArea()));
    }
}

