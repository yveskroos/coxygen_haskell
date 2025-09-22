-- HC8T2 : Types personnalisés et constructeurs de données

-- Type PaymentMethod avec trois constructeurs
data PaymentMethod = Cash | Card | Cryptocurrency
    deriving (Show, Eq)

-- Type Personne avec nom, adresse et mode de paiement
data Personne = Personne
    { nom           :: String
    , adresse       :: (String, Int)  -- Tuple : (rue, numéro)
    , modePaiement  :: PaymentMethod
    } deriving (Show, Eq)

-- Création d'une personne bob qui paie en espèces
bob :: Personne
bob = Personne
    { nom = "yves"
    , adresse = ("Rue Principale", 123)
    , modePaiement = Cash
    }

-- Programme principal
main :: IO ()
main = do
    putStrLn "Informations sur yves :"
    print bob
