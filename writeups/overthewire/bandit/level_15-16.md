# Level 15>16

## Objetivo

Para sacar la contraseña al siguiente nivel hay que subir la contraseña del nivel a localhost por el puerto 30001 usando encriptación SSL/TLS.

## Herramientas usadas

* `openssl`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit15@bandit.labs.overthewire.org -p 2220`
2. Usamos `openssl s_client --connect localhost:30001` para establecer una conexión segura con nosotros mismos por el puerto 30001.
3. Escribimos 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo y nos da la contraseña para el siguiente nivel.

## Password

kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

## Resources

[Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Transport_Layer_Security)

[OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/testing-with-openssl/index.html)

[Cómo usar OpenSSL](https://es.linux-console.net/?p=14816)
