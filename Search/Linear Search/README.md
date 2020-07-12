# Linear Search

## The Code

Basic implementation of linear search:
```Swift
func linearSearch <T: Equatable> (array: [T], object: T) -> Int? {
    for (index, obj) in array.enumerated() where obj == object {
        return index
    }
    return nil
}
```

## Performance
The expected runtime for a linear search is **O(n)**. In a list containing *n* number of elements, the worst-case scenario is when the list doesn't contain our target value or the target is located at the last index. In such cases, *n* number of comparisons will invariably be made - in other words, the runtime is proportional to the length of the list. 

The performance of linear search improves when the target value is more likely to be near the beginning of the list. In particular, when the list items are arranged in order of decreasing probability, and these probabilities are geometrically distributed, the cost of linear search is only **O(1)**.<sup>1</sup>


## Application


## Further Reading
[Wikipedia: Linear Search](https://en.wikipedia.org/wiki/Linear_search)


## References
1: Knuth, Donald (1997). "Section 6.1: Sequential Searching,". Sorting and Searching. The Art of Computer Programming. 3 (3rd ed.). Addison-Wesley. pp. 396–408. ISBN 0-201-89685-0
