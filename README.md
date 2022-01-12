# Swing_P02_compendio
## Tabla de contenidos
1. [Descripcion del proyecto](#descripcion-del-proyecto)
2. [Contenido de la publicacion](#contenido-de-la-publicacion)
3. [Desarrollo del proyecto](#desarrollo-del-proyecto)
4. [Despliegue](#despliegue)
5. [Construido con](#construido-con)
6. [Versionado](#versionado)
7. [Autores](#autores)
8. [Licencia](#licencia)
9. [Recursos adicionales](#recursos-adicionales)
### Descripcion del proyecto
***
Este proyecto consiste en la creacion de una interfaz gráfica que permite gestionar una plataforma de pisos de 
alquiler turistico, siguiendo los estandares basicos de usabilidad
### Contenido de la publicacion
***
* Desarrollo
> Directorio del proyecto 

* Documentacion tecnica
> Javadoc de la aplicacion

* Documentos
> Documento de usabilidad de la aplicacion

* Ejecutable
> Ejecutable de la aplicacion
### Desarrollo del proyecto
***
```
public class Dialogo extends JDialog {

	/** The p 1. */
	private static Panel1 p1;
	
	/** The p 2. */
	public static Panel2 p2;
	
	/** The p 3. */
	public static Panel3 p3;
	
	/** The p 4. */
	public static Panel4 p4;
	
	/** The panel botones. */
	private PanelBotones panelBotones;
	
	/** The layout. */
	private GridBagLayout layout = new GridBagLayout();
	
	/** The constraints. */
	private GridBagConstraints constraints;
	

	/**
	 * Instantiates a new dialogo.
	 */
	public Dialogo() {

		this.setResizable(true);
		this.setTitle("Alta Pisos");
		getContentPane().setBackground(new java.awt.Color(255,250,205));
		this.setLayout(layout);
		constraints = new GridBagConstraints();
		
		// TAMAÑO IGUAL A LA RESOLUCION
		this.setSize(Toolkit.getDefaultToolkit().getScreenSize());

		// ICONOS
		this.setIconImage(new ImageIcon(getClass().getResource("../recursos/logo.png")).getImage());

		// PANELES
		p1 = new Panel1();

		p2 = new Panel2();

		p3 = new Panel3();

		p4 = new Panel4();

		panelBotones = new PanelBotones();

		// CONSTRAINTS
		constraints.fill = GridBagConstraints.HORIZONTAL;
		this.addComponent(p1, 0, 0, 3, 1);
		
		constraints.fill = GridBagConstraints.NONE;
		this.addComponent(panelBotones, 1, 0, 3, 1);

		constraints.weightx = 1000; // puede crecer más ancho
		constraints.weighty = 1; // puede crecer más alto
		constraints.fill = GridBagConstraints.BOTH;
		this.addComponent(p2, 2, 0, 1, 3);
		this.addComponent(p3, 2, 1, 1, 3);
		this.addComponent(p4, 2, 2, 1, 3);
		

		this.setVisible(true);
	}

	/**
	 * Adds the component.
	 *
	 * @param component the component
	 * @param fila the fila
	 * @param columna the columna
	 * @param ancho the ancho
	 * @param alto the alto
	 */
	private void addComponent(Component component, int fila, int columna, int ancho, int alto) {
		constraints.gridx = columna; // set gridx, La columna en la que se
//colocará el componente.

		constraints.gridy = fila; // set gridy, La fila en la que se colocará
//el componente.

		constraints.gridwidth = ancho; // set gridwidth, El número de
//columnas que ocupa el componente.

		constraints.gridheight = alto; // set gridheight, El número de
//filas que ocupa el componente.

		layout.setConstraints(component, constraints);
		this.add(component);
	}

}
```
### Despliegue
***
* Windows
> Solo debes darle dos veces al .jar que te crea la aplicacion y se ejecutara

* Linea de comandos
> java ‘-jar c: rutadelarchivo.jar
### Construido con
***
Eclipse
### Versionado
***
Version 1.0
### Autores
****
**Marina del Aguila Jimenez**
### Licencia
***
EPL (Licencia Publica)
### Recursos adicionales
***
* [Enlace GitHub](https://github.com/Mina-93/Swing_P02_compendio.git)