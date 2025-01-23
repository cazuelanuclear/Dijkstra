# Dijkstra

Benjamín Torres 21.695.698-7


El algoritmo Dijkstra es una técnica de programación para calcular cuál es el camino más corto desde cierto punto a otro dentro de un grafo representado por una matriz ponderada. El presente algoritmo satisface esta definición e incluso permite decidir al usuario cuál es el punto al que le desea calcular el camino más corto. 

int main(): Posee la interfaz inicial y le da la elección al usuario de decidir el objetivo posterior a la lectura del .txt llamado "matriz". Esto se hace por medio de subprograma llamado numeroALetra(), el cual, como su nombre dice, pasa un número dado a una letra desde la A a la Z. Luego se llama al subprograma dijkstra().

dijkstra(): Es el comando principal. En primera instancia genera los diferentes recursos que necesita para llevar a cabo el cálculo. En pocas palabras, primero busca el camino más corto por medio de setCamino(). Este retorna un número de 0 a n-1, y si retorna -1 es porque no hay más caminos y, por ende, no existe ruta más pequeña. Luego entra en un for donde verifica que por cada número de la línea, si este no está visitado y no es 0 (o que tenga una conexión con el i nodo) y que la suma del valor del camino ya existente del nodo anterior con la conexión actual sean menores que el valor del camino más corto preexistente, entonces se cambia el valor y el nodo entra dentro del stack camino, y en el vector de visitados se guarda el padre del vector que se cambió para tener una referencia cuando se deba retornar el stack del camino si es que se llega a la fila del objetivo.

