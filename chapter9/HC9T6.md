-- HC9T6 : Type de données récursif Tweet

-- Définition du type Tweet
data Tweet = Tweet
    { content    :: String
    , likes      :: Int
    , comments   :: [Tweet]  -- Les commentaires sont eux-mêmes des Tweets
    } deriving (Show, Eq)

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
    
    putStrLn "Exemples de Tweets :"
    print tweet1
    print tweet2
