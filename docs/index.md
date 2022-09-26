# Swift



## Swift base

### if let vs guard let

If let and guard let are two conditional operators or condition checker which make our life super easy. Other languages have only `if` as condition checker but swift provides if let as well as guard let also which are operationally same but a bit different in functionality.

`if let` can be used when we are trying to check if an element is present and if present:

    let colors = ["red", "green", "blue"]
        if let index = colors.firstIndex(where: {$0.elementsEqual("green")}) {
            print("green is present in palette at position \(index)")
        } else {
            print("green is not present in palette")
        }

`guard let` can also be used for condition check and it can also unwrap the optional values but it works a bit different from if let. `guard let` is designed to exit the current function, loop, or condition if the check fails.

    func checkColorInPalette() {
        let colors : [String] = ["red", "green", "blue"]
        guard let index = colors.firstIndex(where: {$0.elementsEqual("green")}) else {
            print("green is not present in palette")
            return
        }
    print(print("green is present in palette at position \(index)"))
    $$}

* if let is similar to if condition with the additional functionality of defining let variable where we can do the computation or optional unwrapping.
* guard let is also similar to if let but it focus on the "happy path" means if the condition is not true, code will not execute further in that particular function, loop or condition but it will return, break or throw.
* In if let, the defined let variables are available within the scope of that if condition but not in else condition or even below that.
* In guard let, the defined let variables are not available in the else condition but after that, it's available throughout till the function ends or anything.




