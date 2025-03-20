# Level 14>15

## Objetivo

Para sacar la contraseña al siguiente nivel hay que subir la contraseña del nivel anterior a localhost por el puerto 30001 usando encriptación SSLTLS.

## Herramientas usadas

* `ssh`
* `nc`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit14@bandit.labs.overthewire.org -p 2220`
2. Usamos `nc localhost 30000` para establecer una conexión con nosotros mismos por el puerto 30000.
3. Escribimos MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS y nos da la contraseña para el siguiente nivel.

## Password

8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
