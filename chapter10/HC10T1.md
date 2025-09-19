-- Définition de la classe ShowSimple
class ShowSimple a where
    showSimple :: a -> String

-- Définition d'un type de paiement
data PaymentMethod
    = Cash
    | CreditCard String 
    | PayPal String       
    deriving (Eq, Show)

-- Implémentation de ShowSimple pour PaymentMethod
instance ShowSimple PaymentMethod where
    showSimple Cash              = "Cash"
    showSimple (CreditCard card) = "Credit Card (****" ++ drop (length card - 4) card ++ ")"
    showSimple (PayPal email)    = "PayPal (" ++ email ++ ")"

-- Exemple d'utilisation
main :: IO ()
main = do
    putStrLn $ showSimple Cash
    putStrLn $ showSimple (CreditCard "123812345678")
    putStrLn $ showSimple (PayPal "konanyableyvescharlain@gmail/com")
