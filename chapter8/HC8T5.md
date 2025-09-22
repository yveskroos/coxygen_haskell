-- HC8T5 : Syntaxe d'enregistrement pour Person

-- Définition du type Person avec syntaxe d'enregistrement
data Person = Person
    { name       :: String
    , age        :: Int
    , isEmployed :: Bool
    } deriving (Show, Eq)

-- Création de deux personnes
personne1 :: Person
personne1 = Person
    { name = "Alice"
    , age = 30
    , isEmployed = True
    }

personne2 :: Person
personne2 = Person
    { name = "Bob"
    , age = 25
    , isEmployed = False
    }

-- Programme principal
main :: IO ()
main = do
    putStrLn "Informations sur les personnes :"
    print personne1
    print personne2
