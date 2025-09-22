-- HC8T8 : Synonymes de type et fonction de salutation

-- Synonymes de type
type Name = String
type Age  = Int

-- Fonction de salutation
greet :: Name -> Age -> String
greet name age = "Bonjour " ++ name ++ ", vous avez " ++ show age ++ " ans."

-- Programme principal
main :: IO ()
main = do
    putStrLn "Exemples de salutation :"
    putStrLn (greet "Alice" 30)  -- Résultat : "Bonjour Alice, vous avez 30 ans."
    putStrLn (greet "Bob" 25)    -- Résultat : "Bonjour Bob, vous avez 25 ans."
