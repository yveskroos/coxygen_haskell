-- HC9T7 : Fonction engagement pour Tweet

-- Définition du type Tweet (HC9T6)
data Tweet = Tweet
    { content  :: String
    , likes    :: Int
    , comments :: [Tweet]
    } deriving (Show, Eq)

-- Fonction récursive qui calcule l'engagement total d'un Tweet
engagement :: Tweet -> Int
engagement (Tweet _ likes comments) =
    likes + sum (map engagement comments)

-- Programme principal avec exemple
main :: IO ()
main = do
    -- Tweet sans commentaire
    let tweet1 = Tweet { content = "Hello world!", likes = 10, comments = [] }
    
    -- Tweet avec des commentaires
    let tweet2 = Tweet
            { content = "Mon deuxième tweet"
            , likes = 5
            , comments = [tweet1, Tweet { content = "Super tweet!", likes = 3, comments = [] }]
            }
    
    putStrLn "Engagement total des tweets :"
    print (engagement tweet1)  -- Résultat : 10
    print (engagement tweet2)  -- Résultat : 18 (5 + 10 + 3)
