vertices = [] # en esta linea de codigo se utilizo para al macenar los vertices que se van agregando
contador = 0 # en esta linea de codigo se utilizo para decir que se inicia desde 0 en cada vertice 
while contador < 8: # en esta linea de codigo se utilizo un loop que es un while para decir que solamnete son 8 vertices 
 x, y, z = map(int, input(f"Ingrese las coordenadas del vértice {contador + 1} (x, y, z): ").split()) # en esta linea de codigo se utlizo un map para convertir los vertices en una lista, un int para numeros enteros, el usurio agrege las coordenadas X,Y y Z y  un split para separar cada coordenada
 vertices.append((x, y, z)) # se utilizo append para tener una lista de cad vertice 
 contador += 1 # se utilizo para pasar de un vertice a otro vertice
 caras = {} # se utlizo esto para almacenar las caras 
 nombres_caras = ["Base", "parte superior", "frontal", "lateral izquierda", "lateral derecha", "parte trasera"] # se utilizo para nombrar cada cara
 contador = 0 # iniciar desde 0 para cada cara 
 while contador < 6: # se utilizo un while para deccir que solamente son 6 caras en total
 print(f"Ingrese los cuatro vértices para la cara {nombres_caras[contador]}:") # imprimir cada cara con sus vertices 
  cara = [] # lista de caras agregados para los cuatro vertices que forma una cara
  for _ in range(4): # se utilizo un for y range para decir que solamente se puedo agregar 4 vertices para formar una cara de un cubo
   indice = int(input("Número del vértice (1-8): ")) - 1 # Se solicita el número del vértice y se ajusta a índice de 1 al 8 que se puede tener para cada vertice para formar una cara 
   if 0 <= indice < 8: # se utilizo un if para validar si el indice esta correcto 
   cara.append(vertices[indice]) # se utilizo append para agregar un vertice a la lista de caras 
   else:
            print("Índice inválido, intente de nuevo.") # se utilizo un else para validar si es o no es correcto el indice 
 continue # continuar si es valido y si no es volver a intentarlo
 caras[nombres_caras[contador]] = cara # almacenar caras en una lista con una funcion
 contador += 1 # pasar a la siguiente cara 

 print("Vértices del cubo:")
contador = 0 # iniciar desde 0
while contador < len(vertices):  # longitud de los vertices
    print(f"v{contador + 1}: {vertices[contador]}") # se imprime todas los vertices del cubo

print("Caras del cubo:")
contador = 0 # iniciar desde 0
while contador < len(caras):  # longitud de las caras, y luego se imprime todas las caras del cubo
nombre = list(caras.keys())[contador] # obtener cada nombre de la cara con keys
print(f"c{contador + 1}: {nombre} -> {caras[nombre]}")  # Imprimir la cara con sus vértices
    contador += 1 # la siguiente cara  con su vertice 
# y este es el final de este codigo, explicado detalladamente.
