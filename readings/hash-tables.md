# Hash Tables

Hash tables actually seem really cool. In essence, they are like a huge array, and each index of the array holds a `bucket`.

These buckets are themselves linked lists.

They way this works is that the data that you want to store in the hash table will consist of key / value pairs.

You then create a hash with a determinite hashing algorithm, and use the hash to choose what index in the array that you want to store the key / value pair of data.

This hashing algorithm is determinite for a reason, you want to be able to generate the same hash per key / value pair each time, because you will need it to locate what index it is stored in.

Now becuase of this hashing algorithm, it is possible that some data will wind up being stored at the same index of the table (array). This is called a `collision`.

The workaround for collissions is that previously mentioned fact that the buckets at each index are actually linked lists. This enables us to say we need this data set located at this index, iterate through the linked list to find it.

This entire process allows us to quickly and efficiently store and retrieve large amounts of data without having to iterate over an entire array or other data structure in order to locate it.