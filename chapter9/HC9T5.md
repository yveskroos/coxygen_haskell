-- HC9T5 : Type de données paramétré Shape avec syntaxe d'enregistrement

-- Définition du type paramétré Shape a
data Shape a
    = Circle  { color :: a, radius :: Float }
    | Rectangle { color :: a, width :: Float, height :: Float }
    deriving (Show, Eq)

-- Programme principal avec exemples
main :: IO ()
main = do
    -- Cercle avec couleur String
    let c1 = Circle { color = "Rouge", radius = 5 }
    
    -- Rectangle avec couleur String
    let r1 = Rectangle { color = "Bleu", width = 10, height = 5 }
    
    putStrLn "Exemples de Shape paramétré :"
    print c1  -- Résultat : Circle {color = "Rouge", radius = 5.0}
    print r1  -- Résultat : Rectangle {color = "Bleu", width = 10.0, height = 5.0}
