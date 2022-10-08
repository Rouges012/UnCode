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


class Atencion():
  def __init__(self):
    Info=input().split(" ")
    Info=self.Convertir_Integer(Info)
    self.Ingenieros=Crear_Cola(Info[1])
    self.Usuarios=Crear_Cola(Info[2])
    
    for i in range(Info[1]):
      Ingeniero=input().split()
      Ingeniero=self.Convertir_Integer(Ingeniero)
      self.Ingenieros.Enqueue(Ingeniero)
    
    for j in range(Info[2]):
      Persona=input().split()
      Persona=self.Convertir_Integer(Persona)
      self.Usuarios.Enqueue(Persona)

    for k in range(Info[2]):
      self.Analizis(self.Usuarios.Cola[k])

  def Convertir_Integer(self,Lista):
    Temporal=Crear_Cola(len(Lista))
    for a in Lista:
      Temporal.Enqueue(int(a))
    return Temporal.Cola
    
  def Analizis(self,Usuario_Analizar):
    for r in self.Ingenieros.Cola:
      if r[1]<=Usuario_Analizar[1]<=r[2] and Usuario_Analizar[0]<=r[0]:
        print("YES")
        return
    print("NO")

Prueba=Atencion()
