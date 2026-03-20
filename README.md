# con-genial-
Public class
import java.util.ArrayList;

public class Prueba {
    public static void main(String[] ar) {
        // Creamos una lista que almacena objetos de tipo 'Operacion'
        // (Aunque Operacion sea abstracta, la lista puede guardar a sus "hijas")
        ArrayList<Operacion> lista1 = new ArrayList<Operacion>();

        // Agregamos objetos de las clases Suma y Resta
        lista1.add(new Suma(2, 34));
        lista1.add(new Resta(3, 2));
        lista1.add(new Suma(100, 1));

        // POLIMORFISMO: Recorremos la lista con un for-each
        // El programa sabe qué método 'operar' llamar según el objeto
        for (Operacion op : lista1) {
            op.operar();
            op.imprimir();
        }
    }
}
