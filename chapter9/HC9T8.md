-- HC9T8 : Type de données récursif Sequence

-- Définition du type Sequence a
data Sequence a
    = EmptySeq
    | Node a (Sequence a)
    deriving (Show, Eq)

-- Programme principal avec exemples
main :: IO ()
main = do
    -- Séquence vide
    let seq1 :: Sequence Int
        seq1 = EmptySeq
    
    -- Séquence avec plusieurs nœuds
    let seq2 :: Sequence Int
        seq2 = Node 1 (Node 2 (Node 3 EmptySeq))
    
    putStrLn "Exemples de séquences :"
    print seq1  -- Résultat : EmptySeq
    print seq2  -- Résultat : Node 1 (Node 2 (Node 3 EmptySeq))
