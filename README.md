
1. Create a simple pairRDD of (1, 2), (3, 4), (3, 6).

  val pairRDD = sc.parallelize(List((1,2), (3,4), (3,6))


2. Transform an RDD of ("a","b","c","d","e") to PairRDD (a,0), (b,1), (c,2), (d,3), (e,4)

  val input = sc.parallelize(List(“a”, “b”, “c”, “d”, “e”))
  
  val indexedInput = input.zipWithIndex()
  
  indexedInput.collect
