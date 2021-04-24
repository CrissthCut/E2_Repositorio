# E2_Repositorio
Evidencia de programación avanzada 
# NOTECE QUE EL CODIGO ESTA ELABORADO EN PHYTON, PARA REMARCAR INSTRUCCIONES AQUI, SE HA USADO ESTE CARACTER (#) PARA HACER REFERENCIA A COMENTARIOS EN EL CODIGO.

# Para esta evidencia se presentaran distintos codigos que se vieron durante la fase, por ejemplo ejercicios de listas, listas con diferentes metodos.

# 1.- Para la siguiente lista, utilice el metodo append.

(append agrega el caracter escrito en el parentesis)

versiones_plone=[2.5,3.6,4.5]
print(versiones_plone)

versiones_plone.append(6)
print(versiones_plone)


# 2.- Para la siguiente lista, utilice el metodo remove.

(remove, borra los valores deseados)

versiones_plone=[2.1,2.5,3.6,4,5,6]
print(versiones_plone)

versiones_plone.remove(2.5)
print(versiones_plone)


# 3.- Almacena los valores del 1 al 100 en una lista.

lista = []
i=1
while i<=100:
    lista.append(i)
    i=i+1
print (lista)


# 4.- Pide una cadena por teclado, mete los caracteres en una lista sin espacios.

cadena = input("Dame una cadena: ")
print(cadena)
lista = []
for c in cadena:
    if(c != ' '):
       lista.append(c)
 
print(lista)


# 5.- Escribe un programa que lea una cadena y devuelva una lista con la cantidad de apariciones de cada carácter en la cadena.

dict = {}
cadena = input("Dame una cadena:")
for caracter in cadena:
    if caracter in dict:
        dict[caracter]+=1
    else:
        dict[caracter]=1
for campo,valor in dict.items():
    
    print (campo,"->",valor)
    
    
# 6.- Escribir un programa que almacene las asignaturas de un curso (por ejemplo, Matemáticas, Física, Química, Historia y Lengua) en una lista, pregunte al usuario la nota que ha sacado en cada asignatura, y después las muestre por pantalla con el mensaje En "asignatura" has sacado "nota" donde "asignatura" es cada una des las asignaturas de la lista y "nota" cada una de las correspondientes notas introducidas por el usuario.

asignaturas= ["Matemáticas", "Física", "Química", "Historia", "Lengua"]
notas=[]
for asignatura in asignaturas:
    nota= input("¿Qué nota has sacado en " + asignatura + "? ")
    notas.append(nota)
    
for i in range(len(asignaturas)):
    print("En" + asignaturas[i] + "has sacado: " + notas[i])
    
    
# 7.- Escribir un programa que implemente una agenda. En la agenda se podrán guardar nombres y números de teléfono. El programa nos dará el siguiente menú: Añadir/modificar: Nos pide un nombre. Si el nombre se encuentra en la agenda, debe mostrar el teléfono y, opcionalmente, permitir modificarlo si no es correcto. Si el nombre no se encuentra, debe permitir ingresar el teléfono correspondiente. Buscar: Nos pide una cadena de caracteres, y nos muestras todos los contactos cuyos nombres comiencen por dicha cadena. Borrar: Nos pide un nombre y si existe nos preguntará si queremos borrarlo de la agenda. Listar: Nos muestra todos los contactos de la agenda.Implementar el programa con una lista.

agenda = {}
while True:
    print("\n")
    print("1. Añadir/modificar")
    print("2. Buscar")
    print("3. Borrar")
    print("4. Listar")
    print("5. Salir")
 
 () opcion = int(input("Dime opción:"))
    if opcion == 1:
        nombre = input("Nombre del contacto:")
        if nombre in agenda:
            print("%s ya existe su número de teléfono es %s" % (nombre,agenda[nombre]))
            opcion = input("Pulsa 's' si quieres modificarlo!!!. Otra tecla para continuar.")
            if opcion == "s":
                numero = input("Dame el nuevo número de teléfono:")
                agenda[nombre]=numero
        else:
            numero = input("Dame el número de teléfono:")
            agenda[nombre]=numero
    elif opcion == 2:
        cadena = input("Nombre del contacto a buscar:") 
        for nombre, numero in agenda.items():
            if nombre.startswith(cadena):
                print("El número de teléfono de %s es el %s" % (nombre,agenda[nombre]))
    elif opcion == 3:
        nombre = input("Nombre del contacto para borrar:") 
        if nombre in agenda:
            opcion = input("Pulsa 's' si quieres borrarlo!!!. Otra tecla para continuar.")
            if opcion == "s":
                del agenda[nombre]
        else:
            print("No existe el contacto")
    elif opcion == 4:
        for nombre, numero in agenda.items():
            print(nombre,"->",numero)
    elif opcion == 5:
        break
    else:
        print("Opción incorrecta")



ANA CRISTINA CAVAZOS OYERVIDEZ 


