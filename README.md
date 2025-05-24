# Solucionador de Sudokus
en este proyecto se utilizo Tkinter y Back-Traking, utilice spider 7

# Como lo hice?
primero definí los objetos que hiba a utilizar, el root, self, las celdas, los botones y también agregué una tag que diga que hay que hacer

### Celdas
cree las celdas y sus divisiones 3x3, coloque low y col (columna y línea) para definir sis trayectorias
del Arial de las celdas, su tamaño y color, además de personaliza su anchor y divisiones par aque parezca más un Sudoku

### Botones
en este apartado hice 3 botones, uno para resolver(activando el solve_sudoku)
otro para borrar el ya resuelto y colocar uno nuevo(clear_greed)
y por último uno para poner un ejemplo y ver como funciona para no hacerlo manual siempre(load_example)

### Grids
en este apartado coloque varias cosas, el rango de numeros que se puede poner(1 a 9) y 0 es un espacio en blanco
que sean enteros, la organización, la detección y que cuando se solucione 
la solucion salga en verde y lo ya puesto en rojo(además del Arial)

### Valid
aquí coloqué que las celdas se dividieran en 3 (por cada cuadro de 9x9), puse los message box en cada uno y sus posiciones

### Ve
Ahora es donde aparece la magia de la solución de los sudokus, en este apartado recopila los digitos ingresados
y los soluciona, pero llegaba un punto en el que no seguía porque el programa colocó un dijito mal
así que utilice el back tracking, que lo que hacemos es decirle a ese programa que esa solución está mal
no sirve y retornando para que lo vuelva a hacer hasta conseguirlo

### config botónes
ya por utlimo tenemos la configuración de los botones
-el primero de "resolver", utiliza "Ve" y los "grids" para activarlos
sí no hay ninguna solución posible o el dijito es más de 9 saltará el error
-para "Nuevo sudoku", limpiamos el grid ingresado para colocar un nuevo Sudoku
-el botón "Ejemplo para Resolver", utiliza un ejmeplo predeterminado y
colocando automáticamente en las grids, donde ya antes dicho 0 es en blanco

### Ya por último sólo quedaría iniciar la aplicación:
if __name__ == "__main__":
    root = tk.Tk()
    app = SudokuSolverGUI(root)
    root.mainloop()

# Dificultades
Este proyecto fue algo completamente nuevo para mi, tuve que aprender tkinter
pero lo mas difícil de hacerlo fue aprender a hacer las celdas, los colores
y utilizar el self, también tuve que aprender a hacer el back-traking para poder
hacer funcionar el programa, pero lo más difícil de todo diría yo,
fue poder comprender como funciona cada cosa y como a pesar de saber hacer algo
puede que se necesite algo más para activar ese algo
encontrar las bases para lograrlo y hacerlo bien, prueba y error.
