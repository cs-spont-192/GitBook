# Level 13>14

## Objetivo

Para encontrar la contraseña al siguiente nivel hay que buscar en _/etc/bandit\_pass/bandit14_ y solo podemos leerlo siendo el usuario **bandit14**.

## Herramientas usadas

* `ssh`
* `cd`
* `ls`
* `cat`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit13@bandit.labs.overthewire.org -p 2220`
2. Usamos `cd` para ir navegando hasta entrar en \`/home/bandit14/.
3. Usamos `ls -la` para comprobar los archivos de la carpeta, encontrando **authorized\_keys**.
4. Navegamos de nuevo al directorio principal y haciendo `ls` aparece la llave privada sshkey.private.
5. Nos conectamos como bandit14 usando la clave SSH que acabamos de encontrar `ssh -i sshkey.private bandit14@localhost -p 2220`.
6. Navegamos hasta _/etc/bandit\_pass/bandit14_ y hacemos `cat bandit14` para ver la contraseña.

## Password

MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

## Resources

[SSH/OpenSSH/Keys Ubuntu Help](https://help.ubuntu.com/community/SSH/OpenSSH/Keys).
