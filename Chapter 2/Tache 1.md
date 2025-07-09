HC2T1 - Task 1: Checking Types in GHCi

---

### ✅ CODE COMPLET (Fichier Haskell prêt à l'emploi)

```haskell
-- Fichier : Main.hs

-- Déclaration du module principal
module Main where

-- Fonction qui multiplie un nombre par 2
double :: Int -> Int
double x = x * 2

-- Fonction qui incrémente un nombre de 1
increment :: Int -> Int
increment x = x + 1

-- Fonction composée : applique double, puis increment
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double

-- Fonction main pour tester dans un programme complet
main :: IO ()
main = do
    putStrLn ("double 4 = " ++ show (double 4))
    putStrLn ("increment 4 = " ++ show (increment 4))
    putStrLn ("doubleThenIncrement 4 = " ++ show (doubleThenIncrement 4))
```

---

### ✅ EXÉCUTION

#### Option 1 : Depuis un fichier

1. Sauvegarde ce code dans un fichier nommé `Main.hs`.
2. Dans ton terminal :

   ```bash
   runghc Main.hs
   ```

Tu obtiendras :

```
double 4 = 8
increment 4 = 5
doubleThenIncrement 4 = 9
```

#### Option 2 : Directement dans GHCi

Ligne par ligne dans GHCi :

```haskell
double x = x * 2
increment x = x + 1
doubleThenIncrement = increment . double
doubleThenIncrement 4
```

Résultat :

```haskell
9
```

---
