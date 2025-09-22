-- HC8T7 : Types de données et description d'animaux

-- Définition du type Animal
data Animal = Dog String | Cat String
    deriving (Show, Eq)

-- Fonction qui décrit l'animal
decrireAnimal :: Animal -> String
decrireAnimal (Dog name) = "Chien nommé " ++ name
decrireAnimal (Cat name) = "Chat nommé " ++ name
-- Création d'instances
monChien :: Animal
monChien = Dog "Rex"

monChat :: Animal
monChat = Cat "Miaou"

-- Programme principal
main :: IO ()
main = do
    putStrLn "Description des animaux :"
    putStrLn (decrireAnimal monChien)  -- Résultat : "Chien nommé Rex"
    putStrLn (decrireAnimal monChat)   -- Résultat : "Chat nommé Miaou"
