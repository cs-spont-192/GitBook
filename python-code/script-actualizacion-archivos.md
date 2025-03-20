# Script actualización archivos

## Planteamiento

Imaginemos que contamos con un programa en la empresa que filtra paquetes por IP.&#x20;

**Persona X** de la empresa se limita a ir incluyendo IPs en dos archivos, dependiendo de si son IPs permitidas o no. No entiende de software, ni configuraciones, simplemente va recibiendo direcciones IP que debe meter en una lista o en otra.

Necesitamos automatizar el proceso, y conseguir que automáticamente tengamos un .txt que solamente incluya las direcciones ya actualizadas para poder pasarlo al programa de filtrado.

## Propuesta de Código

{% code fullWidth="true" %}
```python
# Assigning variables to each .txt list

allow_list = "/home/mypc/Documents/allow_list.txt"
deny_list = "/home/mypc/Documents/deny_list.txt"
updated_list = "/home/mypc/Documents/updated_files.txt"

# Reading the allowed IPs file

with open(allow_list, "r") as file:
    allow = file.read()
    allow_sliced = allow.split()

# Reading the denied IPs file

with open(deny_list, "r") as file2:
    deny = file2.read()
    deny_sliced = deny.split()

# Comparing each IP in the allowed list with the denied list
# If an IP exists in the denied IP list, it'll be removed from the allowed list
    
for element in allow_sliced:
    if element in deny_sliced:
        allow_sliced.remove(element)

# Converting the lists into string data

allow_sliced = " ".join(allow_sliced)
deny_sliced = " ".join(deny_sliced)

# Writing the info into an updated file list

with open(updated_list, "w") as updated:
    updated.write(allow_sliced)

# Informing the user about the updated state of allowed/denied IPs 

print("==== LISTA ACTUALIZADA CON ÉXITO ====\n\nIPs Permitidas: " + allow_sliced + "\nIPs Denegadas: " + deny_sliced)
```
{% endcode %}

