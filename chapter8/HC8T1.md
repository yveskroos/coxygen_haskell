-- HC8T1 : Synonymes de type et fonction de base

-- Synonymes de type
type Address = String
type Value   = Int

-- Fonction qui génère une transaction sous forme de chaîne
generateTx :: Address -> Address -> Value -> String
generateTx from to amount =
    "Transaction de " ++ show amount ++
    " de " ++ from ++ " vers " ++ to

-- Programme principal
main :: IO ()
main = do
    putStrLn "Exemples de generateTx :"
    print (generateTx "Alice" "Bob" 50)     -- Résultat : "Transaction de 50 de Alice vers Bob"
    print (generateTx "Charlie" "Dave" 100) -- Résultat : "Transaction de 100 de Charlie vers Dave"
