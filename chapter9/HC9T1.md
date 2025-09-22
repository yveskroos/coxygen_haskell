-- HC9T1 : Synonyme de type paramétrique

-- Synonyme de type paramétrique Entity a
type Address = String
type Entity a = (a, Address)  -- Représente une entité de type 'a' avec une adresse

-- Programme principal avec exemples
main :: IO ()
main = do
    -- Exemple avec une entité de type String
    let user :: Entity String
        user = ("Yves", "123 Rue Principale")
    
    -- Exemple avec une entité de type Int
    let company :: Entity Int
        company = (101, "456 Avenue Centrale")
    
    putStrLn "Exemples d'entités :"
    print user     -- Résultat : ("Alice","123 Rue Principale")
    print company  -- Résultat : (101,"456 Avenue Centrale")
