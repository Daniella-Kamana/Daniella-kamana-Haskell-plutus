HC1T1 - Tâche 1 : Composition de fonctions



```haskell
-- Fonction qui multiplie un nombre par 2
double :: Int -> Int
double x = x * 2

-- Fonction qui augmente un nombre de 1
increment :: Int -> Int
increment x = x + 1

-- Fonction composée : applique double, puis increment
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double

-- Exemple d’utilisation (optionnel, si tu veux tester dans un fichier)
main :: IO ()
main = do
    print (double 5)               -- Résultat attendu : 10
    print (increment 10)          -- Résultat attendu : 11
    print (doubleThenIncrement 5) -- Résultat attendu : 11
```

---

### 📘 **Explication des fonctions**

---

#### 1. `double`

```haskell
double :: Int -> Int
double x = x * 2
```

* **Type** : `Int -> Int` → prend un entier, renvoie un entier.
* **Action** : multiplie l'entrée `x` par `2`.
* **Exemple** : `double 4` donne `8`.

---

#### 2. `increment`

```haskell
increment :: Int -> Int
increment x = x + 1
```

* **Type** : `Int -> Int`
* **Action** : ajoute `1` à l'entrée.
* **Exemple** : `increment 8` donne `9`.

---

#### 3. `doubleThenIncrement`

```haskell
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double
```

* **Type** : `Int -> Int`
* **Action** : applique **d'abord `double`**, puis **`increment`**.
* **Le point `.`** signifie **composition de fonctions**.

💡 **Composition** en Haskell : `(f . g) x = f (g x)`

* Ici : `doubleThenIncrement x = increment (double x)`

* **Exemple** :

  * `doubleThenIncrement 5`
  * `= increment (double 5)`
  * `= increment 10`
  * `= 11`

---
