class Crear_Cola():
    def __init__(self, Tamaño):
        self.Cola = [None] * Tamaño
        self.Capacidad = Tamaño
        self.Puntero = 0

    def Full(self):
        if self.Capacidad == self.Puntero:
            return True
        else:
            return False

    def Empty(self):
        if self.Puntero == 0:
            return True
        else:
            return False

    def Enqueue(self, Valor):
        if self.Full() == False:
            self.Cola[self.Puntero] = Valor
            self.Puntero += 1

    def Desenqueue(self):
        if self.Empty() == False:
            self.Puntero -= 1
            devolver = self.Cola[0]
            for n in range(self.Puntero):
                self.Cola[n] = self.Cola[n + 1]
            self.Cola[self.Puntero] = None
            return devolver


class Repartir_electrodomesticos():
    def __init__(self):
        Intentos = int(input())
        for i in range(Intentos):
            Cantidad_Bruto = int(input())
            self.Electrodomesticos = Crear_Cola(Cantidad_Bruto)
            self.Enlistar()
            self.Desenlistar()

    def Enlistar(self):
        Bruto = input().split(" ")
        for j in Bruto:
            self.Electrodomesticos.Enqueue(j)

    def Desenlistar(self):
        Tiendas = int(input())
        Cantidad_Por_Tiendas = input().split()
        for a in range(Tiendas):
            Cantidad_Por_Tiendas[a] = int(Cantidad_Por_Tiendas[a])

        for p in range(Tiendas):
            Imprimir = "["
            if self.Electrodomesticos.Empty() == False:
                for q in range(Cantidad_Por_Tiendas[p]):
                    if self.Electrodomesticos.Empty() == False:
                        Imprimir += self.Electrodomesticos.Desenqueue()
                        if q < Cantidad_Por_Tiendas[p] - 1 and self.Electrodomesticos.Empty() == False:
                            Imprimir += " "
            Imprimir += "]"
            print(Imprimir)


Inicio = Repartir_electrodomesticos()
