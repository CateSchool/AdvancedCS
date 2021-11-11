# Data Structures

When we're writing code, we need to store data in memory. As we've seen, there are costs (in time and space/ memory) associated with how we store, search, and sort that data. So far we're seen arrays and objects, but there are myriad other **data structures** that facilitate the storage and manipulation of data sets. Different data structures have different properties and different use cases, which we will examine in this unit.


array insert at head
What do you think is the runtime of the insertToHead function? It looks the same as the previous one, except that we are using unshift instead of push. But there’s a catch! unshift algorithm makes room for the new element by moving all existing ones to the next position in the Array. So, it will iterate through all the elements.