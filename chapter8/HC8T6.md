-- HC8T6 : Syntaxe d'enregistrement pour variantes Shape

-- Définition du type Shape avec syntaxe d'enregistrement
data Shape
    = Circle
        { center :: (Float, Float)
        , color  :: String
        , radius :: Float
        }
    | Rectangle
        { width  :: Float
        , height :: Float
        , color  :: String
        }
    deriving (Show, Eq)

-- Programme principal
main :: IO ()
main = do
    -- Exemple de cercle
    let c = Circle { center = (0,0), color = "Rouge", radius = 5 }
    
    -- Exemple de rectangle
    let r = Rectangle { width = 10, height = 5, color = "Bleu" }
    
    putStrLn "Exemples de formes :"
    print c
    print r
