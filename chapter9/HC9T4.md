-- HC9T4 : Fonction extract pour Box

-- Définition du type Box (HC9T2)
data Box a = Empty | Has a
    deriving (Show, Eq)

-- Fonction qui extrait la valeur ou retourne une valeur par défaut
extract :: a -> Box a -> a
extract def Empty   = def
extract _   (Has x) = x

-- Programme principal avec exemples
main :: IO ()
main = do
    let emptyBox :: Box Int
        emptyBox = Empty
    
    let fullBox :: Box Int
        fullBox = Has 42
    
    putStrLn "Exemples de extract :"
    print (extract 0 emptyBox)  -- Résultat : 0
    print (extract 0 fullBox)   -- Résultat : 42
