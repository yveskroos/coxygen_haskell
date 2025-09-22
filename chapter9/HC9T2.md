-- HC9T2 : Type de données paramétré Box

-- Définition du type Box avec deux constructeurs
data Box a = Empty | Has a
    deriving (Show, Eq)

-- Programme principal avec exemples
main :: IO ()
main = do
    let emptyBox :: Box Int
        emptyBox = Empty
    
    let fullBox :: Box String
        fullBox = Has "Cadeau"
    
    putStrLn "Exemples de Box :"
    print emptyBox  -- Résultat : Empty
    print fullBox   -- Résultat : Has "Cadeau"
