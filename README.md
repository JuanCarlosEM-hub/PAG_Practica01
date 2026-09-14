# PROGRAMACIÓN DE APLICACIONES GRÁFICAS
## Práctica 1: Configuración
> Juan Carlos Enríquez Muñoz

### Ejercicio de Reflexión

**1. ¿Cómo debería declararse el objeto de la clase PAG::Renderer que actúa como
renderer de la aplicación?**

En este caso, la mejor forma de gestionar el objeto sería con un puntero inteligente `std::unique_ptr<PAG::Renderer>`.  
De esta forma podríamos gestionar de forma automática la memoria ya que, al destruirse la ventana, la memeoria del rederizado se libera sola sin usar _delete_

**2. ¿Qué módulo de la aplicación debería inicializarlo?**

Debería de inicializarse en el modulo principal de control de la aplicación, en nuestro caso, el fichero `main.cpp`