-- HC8T3 : Types algébriques et fonction Area

-- Définition du type Shape
data Shape = Circle Float | Rectangle Float Float
    deriving (Show, Eq)

-- Fonction qui calcule l'aire d'une forme
area :: Shape -> Float
area (Circle r)       = pi * r * r
area (Rectangle l h)  = l * h

-- Programme principal
main :: IO ()
main = do
    -- Création des formes
    let cercle = Circle 5
    let rectangle = Rectangle 10 5
    
    -- Calcul et affichage des aires
    putStrLn $ "Aire du cercle (r=5) : " ++ show (area cercle)       -- Résultat : 78.53982
    putStrLn $ "Aire du rectangle (10x5) : " ++ show (area rectangle) -- Résultat : 50.0
