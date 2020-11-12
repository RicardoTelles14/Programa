import java.util.Scanner;
class Main{
public static void main(String[] args){
Scanner inp = new Scanner(System.in);
int matriz [][], filas, columnas;
Autores();
System.out.println("Numero de filas ");
filas = inp.nextInt();
System.out.println("Numero de columnas ");
columnas = inp.nextInt();
matriz = new int [filas] [columnas];
Matriz m1 = new Matriz(filas,columnas,matriz);
m1.Datos();
m1.imprimirMatriz();
}
public static void Autores(){
System.out.println("\nAutores: Julio, Fernando, Ricardo");
}
}
class Matriz{
int matriz[][], filas, columnas;
public Matriz(int filas,int columnas,int matriz[][]){
this.filas = filas;
this.columnas = columnas;
this.matriz = matriz;
}
public void Datos(){
Scanner dato = new Scanner(System.in);
for (int n=0; n < filas; n++) {
for (int m=0; m < columnas; m++) {
System.out.println("Ingrese el elemento ["+(n+1)+"] ["+(m+1)+"]: ");
matriz[n][m]= dato.nextInt();
}
}
}
public void imprimirMatriz(){
for (int i=0; i < filas; i++) {
for (int j=0; j < columnas; j++) {
System.out.print(matriz[i][j] + " ");
}
System.out.println();
}
}
}
