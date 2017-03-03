# Empleado
Cree una clase de tipo abstract Empleado en donde se pueda calcular el salario de este empleado. 

public abstract class Empleado {
 
    protected final static double SALARIO_DEF=600;
 
    protected String nombre;
    
    protected String apellido;
    
    protected int edad;
    
    protected double salario;
 
    public String getNombre() {
        return nombre;
    }
 
    
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
 
    
    public int getEdad() {
        return edad;
    }
 
    
    public void setEdad(int edad) {
        this.edad = edad;
    }
 
    public double getSalario() {
        return salario;
    }
 
    
    public  void setSalario(double salario) {
        this.salario = salario;
    }
 
    public abstract boolean plus (double sueldoPlus);
 
    
    public Empleado(){
        this ("", "", 0, SALARIO_DEF);
    }
 
    
    public Empleado(String nombre, String apellido, int edad, double salario){
        this.nombre=nombre;
        this.apellido=apellido;
        this.edad=edad;
        this.salario=salario;
    }
}

// clase hija de Empleado

public class Comercial extends Empleado{
 
    public boolean plus (double sueldoPlus){
 
        boolean aumento=false;
        if (comision<50){
            salario+=sueldoPlus;
            aumento=true;
        }
        return aumento;
    }
 
    
    public Comercial(){
         super();
        this.comision=0;
    }
 
    
    public Comercial(String nombre, String apellido, int edad, double salario, double comision) {
        super(nombre, apellido, edad, salario);
        this.comision=comision;
    }
}
// Clase de inicio

public class EmpleadoApp {
 
    public static void main(String[] args) {
 
        Comercial comercial1=new Comercial();
    }
 
}

