import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

// Clase base para representar un usuario

class Usuario {
    private String nombreCompleto;

    private String correoElectronico;

    private String codigoPerfil;

    public Usuario(
            String nombreCompleto, String correoElectronico, String codigoPerfil) {
        this.nombreCompleto = nombreCompleto;

        this.correoElectronico = correoElectronico;

        this.codigoPerfil = codigoPerfil;
    }

    // Método para mostrar información básica del usuario

    public void mostrarContenido() {
        System.out.println("Nombre completo: " + nombreCompleto);

        System.out.println("Correo electrónico: " + correoElectronico);

        System.out.println("Código de perfil: " + codigoPerfil);
    }
}

// Clase para representar un Administrador

class Administrador extends Usuario {
    private String claveAdministrador;

    public Administrador(String nombreCompleto, String correoElectronico,
                         String codigoPerfil, String claveAdministrador) {
        super(nombreCompleto, correoElectronico, codigoPerfil);

        this.claveAdministrador = claveAdministrador;
    }

    // Método para mostrar información específica del Administrador

    @Override

    public void mostrarContenido() {
        super.mostrarContenido();

        System.out.println("Acciones disponibles: asignarCodigoAPerfil()");
    }
}

// Clase para representar un Cajero

class Cajero extends Usuario {
    private String claveCajero;

    public Cajero(String nombreCompleto, String correoElectronico,
                  String codigoPerfil, String claveCajero) {
        super(nombreCompleto, correoElectronico, codigoPerfil);

        this.claveCajero = claveCajero;
    }

    // Método para mostrar información específica del Cajero

    @Override

    public void mostrarContenido() {
        super.mostrarContenido();

        System.out.println("Acciones disponibles: registrarVenta()");
    }
}

// Clase para representar un Cliente

class Cliente extends Usuario {
    private String telefonoContacto;

    private String direccionContacto;

    public Cliente(String nombreCompleto, String correoElectronico,
                   String codigoPerfil, String telefonoContacto, String direccionContacto) {
        super(nombreCompleto, correoElectronico, codigoPerfil);

        this.telefonoContacto = telefonoContacto;

        this.direccionContacto = direccionContacto;
    }

    // Método para mostrar información específica del Cliente

    @Override

    public void mostrarContenido() {
        super.mostrarContenido();

        System.out.println("Acciones disponibles: consultarProductos()");

        System.out.println("Teléfono de contacto: " + telefonoContacto);

        System.out.println("Dirección de contacto: " + direccionContacto);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Usuario> listaUsuario = new ArrayList<Usuario>();
        while(true) {
            System.out.println("Menú de Registro de Usuario");
            System.out.println("1. Registrar Usuario");
            System.out.println("2. Mostrar Contenido");
            System.out.println("3. Salir");

            System.out.println("Digite una opción:  ");
            int opcion = scanner.nextInt();

            switch (opcion)
            {
                case 1:
                    System.out.println("Ingrese el nombre del usuario: ");
                    String nombreCompleto = scanner.next();
                    System.out.println("Ingrese el correo electrónico del usuario: ");
                    String correo = scanner.next();
                    System.out.println("Ingrese el código del tipo de usuario: ");
                    String codigoPerfil = scanner.next();
                    if(codigoPerfil.equalsIgnoreCase("1")){
                        System.out.println("Ingrese la clave del administrador: ");
                        String claveAdmon = scanner.next();
                        Administrador admon = new Administrador(nombreCompleto, correo, codigoPerfil, claveAdmon);
                        listaUsuario.add(admon);
                    }else if(codigoPerfil.equalsIgnoreCase("2")){
                        System.out.println("Ingrese la clave del cajero: ");
                        String claveCajero = scanner.next();
                        Cajero cajero = new Cajero(nombreCompleto, correo, codigoPerfil, claveCajero);
                        listaUsuario.add(cajero);
                    }else{
                        System.out.println("Ingrese el teléfono de contacto del cliente: ");
                        String telefonoContacto = scanner.next();
                        System.out.println("Ingrese la dirección de contacto del cliente: ");
                        String direccionContacto = scanner.next();
                        Cliente cliente = new Cliente(nombreCompleto, correo, codigoPerfil, telefonoContacto, direccionContacto);
                        listaUsuario.add(cliente);
                    }
                    break;
                case 2:
                    System.out.println("A continuación se muestra el contenido de los usuarios registrados: ");
                    for(Usuario usuario:listaUsuario){
                        usuario.mostrarContenido();
                    }
                    break;
                case 3:
                    System.exit(0);

                default:
                    System.out.println("Opción invalida. Seleccione una opción válida \n\n");
            }
            
        }
  
    }
}
