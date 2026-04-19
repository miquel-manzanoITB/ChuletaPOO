# 🧠 CHULETA OOP + UML + C#

---

## 🔹 1. Conceptes clau OOP

### 📌 Què és OOP?
- Paradigma que agrupa dades + comportament en objectes  
- Un programa = conjunt d’objectes que interactuen  

---

### 📌 Classe vs Objecte
- **Classe** → plantilla (atributs + mètodes)  
- **Objecte** → instància de la classe  

**Característiques:**
- State → atributs  
- Behaviour → mètodes  
- Identity → identificador únic  

---

### 📌 Propietats clau
- **Abstracció** → mostrar només el necessari  
- **Encapsulament** → protegir dades  
- **Modularitat** → objectes reutilitzables  
- **Herència** → jerarquia (IS-A)  
- **Polimorfisme** → mateix mètode, comportament diferent  

---

### 📌 Encapsulament
**Modificadors d’accés:**
- `public`
- `private`
- `protected`
- `internal`

👉 No accedir directament als atributs → usar getters/setters  

---

### 📌 Herència
- Relació **IS-A**
- Subclasse hereta de superclasse  
- C# → només herència simple  

---

### 📌 Polimorfisme
- **Overloading** → mateix nom, diferents paràmetres  
- **Overriding** → redefinir mètode heretat  

---

### 📌 Classes abstractes
- No es poden instanciar  
- Mètodes sense implementar  
- Subclasses obligades a implementar-los  

---

### 📌 Interfícies
- Contracte de mètodes  
- Sense implementació  
- Permeten herència múltiple en C#  

---

## 🔹 2. UML

### 📌 Què és UML?
- Llenguatge gràfic per modelar sistemes OOP  

---

## 🔸 Diagrama de classes

### 📌 Mostra:
- Classes
- Atributs
- Mètodes
- Relacions  

---

### 📌 Estructura

Classe

atributs

mètodes


---

### 📌 Visibilitat
- `+` public  
- `-` private  
- `#` protected  

---

### 📌 Relacions

#### ✔ Associació
- Relació simple  
- Línia contínua  

#### ✔ Agregació (HAS-A dèbil)
- Parts independents  
- Rombe buit  

#### ✔ Composició (HAS-A fort)
- Parts dependents  
- Rombe ple  

#### ✔ Herència (IS-A)
- Fletxa buida  

#### ✔ Interfície
- Línia discontínua  

---

## 🔸 Diagrama de casos d’ús

### 📌 Mostra:
- Interacció usuari ↔ sistema  

---

### 📌 Elements
- **Actor** → usuari o sistema extern  
- **Cas d’ús** → funcionalitat  
- **Sistema** → rectangle  

---

### 📌 Relacions
- Associació → línia actor-cas  
- Include → sempre s’executa  
- Extend → només en certs casos  
- Generalització → herència  

---

### 📌 Idea clau
👉 Punt de vista de l’usuari  

---

## 🔹 3. C#

## 🔸 Definició de classe
```csharp
public class Car
{
    private int year;
    private double price;

    public Car(int year, double price)
    {
        this.year = year;
        this.price = price;
    }

    public double CalculatePrice()
    {
        if (year < 2000)
            price -= price * 0.2;
        return price;
    }
}
```
---

### 🔸 Propietats
```
public string Name { get; set; }
```

---

###🔸 Controladora (Main)

```csharp
public class Program
{
    public static void Main()
    {
        Car car = new Car(1999, 400000);
        Console.WriteLine(car.CalculatePrice());
    }
}
```

---

###🔸 Passos examen
Llegir enunciat / diagrama
Crear classes
Afegir atributs
Crear constructor
Crear mètodes
Main:
instanciar objectes
cridar mètodes

---

###🔥 Consells
IS-A → herència
Té/un → composició o agregació
Encapsular sempre
UML:
rombe ple = composició
rombe buit = agregació
C#:
new = instància
: = herència


