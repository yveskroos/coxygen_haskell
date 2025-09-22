-- HC9T3 : Fonction addN pour Box

-- Définition du type Box (HC9T2)
data Box a = Empty | Has a
    deriving (Show, Eq)

-- Fonction qui ajoute n à la valeur de la Box si elle n'est pas vide
addN :: Num a => a -> Box a -> Box a
addN _ Empty     = Empty
addN n (Has x)   = Has (x + n)

-- Programme principal avec exemples
main :: IO ()
main = do
    let emptyBox :: Box Int
        emptyBox = Empty
    
    let fullBox :: Box Int
        fullBox = Has 10
    
    putStrLn "Exemples d'addN :"
    print (addN 5 emptyBox)  -- Résultat : Empty
    print (addN 5 fullBox)   -- Résultat : Has 15
