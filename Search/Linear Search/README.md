# Linear Search
___

## The Code
___

```Swift
func linearSearch <T: Equatable> (array: [T], object: T) -> Int? {
    for (index, obj) in array.enumerated() where obj == object {
        return index
    }
    return nil
}
```

## Performance
___
