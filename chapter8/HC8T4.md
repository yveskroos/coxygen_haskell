-- HC8T4 : Syntaxe d'enregistrement pour Employee

-- Définition du type Employee avec syntaxe d'enregistrement
data Employee = Employee
    { name              :: String
    , experienceInYears :: Float
    } deriving (Show, Eq)

-- Création d'un employé Richard avec 7,5 ans d'expérience
richard :: Employee
richard = Employee
    { name = "Richard"
    , experienceInYears = 7.5
    }

-- Programme principal
main :: IO ()
main = do
    putStrLn "Informations sur l'employé :"
    print richard
