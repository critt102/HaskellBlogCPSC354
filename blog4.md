# Beginner Haskell Grammar: Lists
## Blog 4

In my research learning about the basics of Haskell, I found a lot of information about lists. Lists are an important function in any coding language, so it is important to have knowledge of how lists function in Haskell, and the different functions that can be applied to lists. This is a summary of the information I found about lists in Haskell.

> - Lists are homogenous, so they can only contain items of one data type
> - ++ - concatenates a list
> -    -ex. [1,2,3,4] ++ [9,10,11] will return [1,2,3,4,9,10,11]
> - : (cons operator) - puts something at the beginning of a list
> -    -ex. 5:[1,2,3,4] will return [5,1,2,3,4]
> - Both of these functions work with strings as well
> -   -ex. ‘A’ : “ Small Cat” or “hello” ++ “world”
> - !! - gets element out of a list by index (index starts at 0)
> -    -ex. [9,10,11,12,13] !! 1 returns 10
> - Comparing lists using <, >, <=, >= - look at first object in each list to determine True or False
> -    -if the first objects are equal, then it will look at the second, and so on
> - 
> - ### List Functions
> - head - returns first element of list
> -    -if list is empty, there will be an error
> - last - returns last element
> - init - returns everything except last element
> - length - returns length of list
> - null - checks if list is empty, returns True or False
> - reverse - reverses a list
> - take - extracts a given number of elements from the beginning of a list
> -    -ex. take 3 [5,4,3,2,1] returns [5,4,3]
> - drop - drops the number of elements from the beginning of a list (opposite return of take)
> - maximum - returns the biggest element
> - minimum - returns the smallest element
> - sum - returns the product of numbers in a list
> - elem - checks if a given element is in a list, returns True or False
> -    -ex. elem 4 [2,4,5,6] or 4 `elem` [2,4,5,6] will return True
> - .. - used to create ranges
> -    -ex. [1..20] will create a list with elements 1 through 20
> -    -can also specify a step (only one step), ex. [3,6..20] will return all elements that are multiples of three, so [3,6,9,12,15,18] (notice it doesn’t include 20)
> -    -decimals can cause issues with ranges, so best to not use them
> -
> - ###Infinite lists
> - take and .. - get a certain number of multiples
> -    -ex. take 24 [13, 26] will give you the first 24 multiples of 13 in a list
> - cycle - takes a list and cycles it infinitely, use take to cut it off somewhere
> - repeat - produces an infinite list of a single element, use take to cut it off
> - replicate - replicates some number of the same element
> -    -ex. replicate 3 10 returns [10,10,10]
