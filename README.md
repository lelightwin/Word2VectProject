This is an adaptation of English word2Vect to Vietnamese.
Main usage class:
	WordVectorizer
Code to use:
		WordVectorizer vectorizer = new WordVectorizer();
        vectorizer.loadModel(System.getProperty("user.dir"));
        System.out.println(Arrays.toString(vectorizer.vectorFrom("con_trai"))); // get double vector from a word
        System.out.println(vectorizer.vec().similarity("thắng", "bại")); // to check the similarity between two word which is normalized from 0 to 1
        System.out.println(vectorizer.vec().wordsNearest("xe_máy", 10)); // get 10 nearest words to a word, if a word is not existed in corpus, it will return nullpointerexception
