# Radix Sort

## The Code
```Swift
func radixSort(_ array: inout [Int]) {

    var temp = [[Int]](repeating: [], count: 10)

    for num in array { temp[num % 10].append(num) }

    for i in 1...Int(array.max()!.description.characters.count) {

        for index in 0..<temp.count {

            for num in temp[index] {
                temp[index].remove(at: temp[index].index(of: num)!)
                temp[(num / Int(pow(10, Double(i)))) % 10].append(num)
            }
        }
    }
    array = temp[0]
}
```
