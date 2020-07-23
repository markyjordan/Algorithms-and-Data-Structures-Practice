# Quick Sort

## The Code
```Swift
func quickSort<T: Comparable>(_ array: [T]) -> [T] {
  guard array.count > 1 else { return aarray }

  let pivot = array[array.count/2]
  let less = array.filter { $0 < pivot }
  let equal = array.filter { $0 == pivot }
  let greater = array.filter { $0 > pivot }

  return quickSort(less) + equal + quickSort(greater)
}
