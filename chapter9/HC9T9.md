-- HC9T9 : Vérifier la présence d'un élément dans une Sequence

-- Définition du type Sequence (HC9T8)
data Sequence a
    = EmptySeq
    | Node a (Sequence a)
    deriving (Show, Eq)

-- Fonction qui vérifie si un élément est présent dans la séquence
elemSeq :: Eq a => a -> Sequence a -> Bool
elemSeq _ EmptySeq       = False
elemSeq x (Node y rest)
    | x == y    = True
    | otherwise = elemSeq x rest

-- Programme principal avec exemples
main :: IO ()
main = do
    let seq1 = Node 1 (Node 2 (Node 3 EmptySeq))
    
    putStrLn "Vérification de la présence d'éléments dans la séquence :"
    print (elemSeq 2 seq1)  -- Résultat : True
    print (elemSeq 5 seq1)  -- Résultat : False
