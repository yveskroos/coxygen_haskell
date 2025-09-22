-- HC8T9 : Type enregistrement Transaction et fonction associée

-- Synonymes de type
type Address = String
type Value   = Int

-- Définition du type Transaction
data Transaction = Transaction
    { from          :: Address
    , to            :: Address
    , amount        :: Value
    , transactionId :: String
    } deriving (Show, Eq)

-- Fonction qui crée une transaction et retourne son ID
createTransaction :: Address -> Address -> Value -> String
createTransaction sender recipient value =
    let txId = "TX-" ++ sender ++ "-" ++ recipient ++ "-" ++ show value
        _transaction = Transaction
            { from = sender
            , to = recipient
            , amount = value
            , transactionId = txId
            }
    in txId

-- Programme principal
main :: IO ()
main = do
    putStrLn "Exemple de création de transaction :"
    let txId = createTransaction "Yves" "kroos" 50
    putStrLn ("ID de la transaction : " ++ txId)  -- Résultat : "TX-Alice-Bob-50"
