# Level 16>17

## Objetivo

Para sacar la contraseña al siguiente nivel hay que subir la contraseña del nivel a localhost por un puerto en el rango 31000-32000 usando SSL/TLS.

## Herramientas usadas

* `nmap`
* `ssh`
* `openssl`
* `touch`
* `cd`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit16@bandit.labs.overthewire.org -p 2220`
2. Usamos `nmap localhost -p31000-32000 --open -v` para escanear los puertos abiertos e intentar ver los servicios que corren.
3. Vamos probando los 5 puertos hasta dar con el correcto `openssl s_client localhost:31790 -ign_eof.`
4. Nos devuelve una clave RSA, así que hacemos `cd`  para crear una carpeta temporal.
5. Creamos un nuevo archivo, por ejemplo **pk.key.**&#x20;
6. Pegamos la clave RSA en él.
7. Cambiamos los permisos del archivo con `chmod 700 pk.key`.
8. Nos conectamos usando la clave que hemos encontrado `ssh -i pk.key bandit17@localhost -p 2220` .

## Password

16: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

## Resources

[Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Transport_Layer_Security)

[OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/testing-with-openssl/index.html)

[Cómo usar OpenSSL](https://es.linux-console.net/?p=14816)
