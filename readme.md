# 🎰 Fondo Royale - Casino App (TFG)

Bienvenido al repositorio de **Fondo Royale**, una aplicación de casino completa desarrollada como Trabajo de Final de Grado (DAM). Este proyecto simula un ecosistema de apuestas con gestión de usuarios, saldo y múltiples juegos de azar.

El proyecto está estructurado como un **Monorepo** que contiene tanto el servidor (Backend) como la aplicación móvil (Frontend).

## 🚀 Estructura del Proyecto

* **`/backend`**: API REST desarrollada con **Java** y **Spring Boot**. Se encarga de la lógica de negocio, gestión de usuarios, transacciones y persistencia de datos.
* **`/frontend`**: Aplicación nativa Android desarrollada con **Kotlin**. Interfaz de usuario moderna y consumo de la API.

## 🛠️ Tecnologías Utilizadas

* **Backend:** Java 17, Spring Boot, Maven, MySQL (o la BBDD que usaste, Hibernate/JPA).
* **Frontend:** Kotlin, Jetpack Compose (si lo usaste) o XML Views, Retrofit (para llamadas HTTP), Coroutines.
* **Herramientas:** Android Studio, IntelliJ IDEA, Postman.

## 📋 Pre-requisitos

Para ejecutar este proyecto localmente necesitas:
1.  **JDK 17** o superior instalado.
2.  **Android Studio** (Koala o superior recomendado).
3.  **MySQL Database** (asegúrate de crear la base de datos con el nombre configurado en `application.properties`).

---

## ⚙️ Guía de Instalación y Ejecución

⚠️ **IMPORTANTE:** Para que la aplicación móvil funcione, el **Backend debe estar ejecutándose primero**, ya que la app necesita conectarse al servidor para realizar el login y cargar datos.

### Paso 1: Configurar y Ejecutar el Backend

1.  Navega a la carpeta del backend:
    ```bash
    cd backend
    ```
2.  Configura tu base de datos en `src/main/resources/application.properties` (usuario y contraseña de tu MySQL).
3.  Ejecuta la aplicación usando Maven:
    * **Windows:**
        ```cmd
        mvnw.cmd spring-boot:run
        ```
    * **Mac/Linux:**
        ```bash
        ./mvnw spring-boot:run
        ```
4.  El servidor debería iniciar en el puerto `8080` (por defecto).

### Paso 2: Ejecutar el Frontend (Android)

1.  Abre **Android Studio**.
2.  Selecciona **Open** y navega a la carpeta `/frontend` de este repositorio.
3.  Deja que Gradle sincronice las dependencias.
4.  **Configuración de IP (Crucial):**
    * Si usas el **Emulador de Android**, asegúrate de que la URL base en tu código (probablemente en `RetrofitClient` o `Constants`) apunte a `http://10.0.2.2:8080`. Esta es la dirección especial que usa el emulador para referirse al `localhost` de tu ordenador.
    * Si usas un **Dispositivo Físico**, asegúrate de que tu móvil y tu PC estén en la misma red WiFi y usa la IP local de tu PC (ej: `192.168.1.XX:8080`).
5.  Dale al botón de **Run (▶)** en Android Studio.

## 📱 Funcionalidades Principales

* **Autenticación:** Login y Registro de usuarios contra base de datos.
* **Perfil:** Gestión de saldo, niveles y estadísticas.
* **Juegos:**
    * 🃏 BlackJack
    * 🎰 Slot Machine
    * 🔴 Ruleta
    * 🎫 Rasca y Gana

## Contribuidores
Joan Albert Chias
Gerard Bartalot
Sergio Arenas
Nil Arroyo
