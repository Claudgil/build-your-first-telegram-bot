# 🤖 Build Your First Telegram Bot with Python

¡Bienvenidxs! Este repositorio contiene el código base para la charla **"De idea a bot: crea tu primer Telegram bot con Python"** presentada en la ExpoTecnológica.

## 🚀 ¿Qué hace este bot?

Es un bot minimalista construido con **Flask** que utiliza **Webhooks** para recibir mensajes en tiempo real.

-   Responde al comando `/start` con un saludo personalizado.    
-   Hace "eco" de cualquier mensaje que reciba, demostrando la conexión bidireccional.    

## 🛠️ Stack Tecnológico

-   **Python**: El lenguaje motor.    
-   **Flask**: Micro-framework para manejar las peticiones web (Webhooks).    
-   **Telegram Bot API**: El puente de comunicación con el usuario.    
-   **ngrok**: Para crear un túnel seguro desde tu `localhost` hacia el mundo exterior.    

----------

## 🏃‍♀️ Cómo empezar

### 1. Requisitos previos

-   Tener instalado Python 3.x.
-   pip  
-   Una cuenta de Telegram.    
-   **ngrok** instalado en tu máquina.
    

2. Configuración del Bot (BotFather)

1.  Busca a `@BotFather` en Telegram.    
2.  Usa el comando `/newbot` y sigue las instrucciones para obtener tu **API TOKEN**.
    

### 3. Instalación local

Bash

```
# Clonar el repo 
git clone https://github.com/tu-usuario/build-your-first-telegram-bot.git
cd build-your-first-telegram-bot

# Instalar dependencias
pip install -r requirements.txt

```

### 4. Ejecución

1.  Define tu token en una variable por seguridad:
    
    Bash
    
    ```
    export TELEGRAM_TOKEN="tu_token_aqui"
    
    ```
    
2.  Corre la aplicación Flask:
    
    Bash
    
    ```
    python app.py
    
    ```
    
3.  En otra terminal, levanta ngrok:
    
    Bash
    
    ```
    ngrok http 5000
    
    ```
    
4.  Configura el Webhook de Telegram usando la URL de ngrok:
    
    Bash
    
    ```
    curl -X POST https://api.telegram.org/bot$TELEGRAM_TOKEN/setWebhook?url=https://TU_URL_NGROK.ngrok-free.app/webhook
    
    ```
    

----------

## 👩‍💻 Sobre la autora

**Veruzka Borges** - Senior Python & Cloud Engineer. Desarrollé este proyecto como parte de una charla para inspirar a más mujeres a entrar al mundo de la automatización y la infraestructura en la nube.
