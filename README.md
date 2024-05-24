# Proxy Inverso con NGINX para Página de Currículum en GitHub

Este repositorio contiene instrucciones detalladas para configurar un proxy inverso utilizando NGINX para tu página de currículum alojada en GitHub. Un proxy inverso te permite redirigir el tráfico de un dominio a otro, lo que es útil para enmascarar la URL de tu sitio o para proporcionar funcionalidades adicionales.

## Pasos

### 1. Instalación de NGINX

Asegúrate de tener NGINX instalado en tu servidor Ubuntu. Si no lo tienes instalado, puedes hacerlo con el siguiente comando:

```bash
sudo apt-get update
sudo apt-get install nginx
```
### 2. Modificación de la configuración de NGINX

Una vez que NGINX esté instalado, debes configurar el archivo de configuración para tu proxy inverso. Puedes encontrar este archivo en /etc/nginx/sites-available/. Es importante que esta carpeta esté vinculada a /sites-enabled para que funcione correctamente. Si no aparece lo mismo en ambas carpetas ejecute el siguiente comando: **sudo ln -s /etc/nginx/sites-available/mi-sitio /etc/nginx/sites-enabled/**

### 3. Accede al sitio WEB que has creado previamente y has guardado en esa carpeta

En mi caso es una página WEB creada con MKDocs y subida utilizando GitHub Pages, y lo que haré con ella es que también sea accesible en mi equipo a través del enlace "sergioweb.com". El código de configuración tendría la siguiente forma:

![nginx](imagenes/imagen1.png)

### 4. Por último lo que haremos será iniciar NGINX, activarlo y comprobar que funciona correctamente.

Los comandos a ejecutar serán los siguientes:
```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```
Y posteriormente si queremos realizar una previa comprobación de que esta todo correcto sin fallos podemos ejecutar el siguiente:
```bash
sudo nginx -t
```




