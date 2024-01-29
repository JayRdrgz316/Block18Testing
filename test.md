# Prompts
1. A function called `multiplication` that returns the product of the two input numbers.
2. A function called `concatOdds` takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both of the arrays.
3. A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.

# Unit Tests:
 `multiplication`

* Expect `multiplication(1, 0)` to equal 0
* Expect `multiplication(0, 0)` to equal 0
* Expect `multiplication(2, 2)` to equal 4
* Expect `multiplication(1, 4)` to equal 4
* Expect `multiplication(1, 10)` to equal 10
* Expect `multiplication(2, 5)` to equal 10
* Expect `multiplication("1", "0")` to equal -1
* Expect `multiplication("2", 2)` to equal -1
* Expect `multiplication(1, "10")` to equal -1


`concatOdds`

* `concatOdds([1,2,3])` to equal `[1, 3, 5]`
* `concatOdds([1,2,3,], [7])` to equal `[1, 3, 7,]`
* `concatOdds([1,2,3,8,7,11], [])` to equal `[1, 3, 7, 11]`
* `concatOdds([], [9,7,13])` to equal `[7, 9, 13]`
* `concatOdds([1,3,2], [9,7,13])` to equal `[1, 3, 7, 9, 13]`


# Functional Tests:
When a user clicks "checkout" in the shopping cart
User will see a message asking if they wish to "create an account", "login" or "check out as guest"

When a user without an account "checks out" in the shopping cart
User clicks "continue as a guest"
Then user can fulfill order entering information manually

When a user without an account clicks "checkout" in the shopping cart
User clicks "create an account"
User is prompted to enter personal information
User completes account with items saved and able to be purchased
For next purchase user can remained signed in for faster checkout

When a user with an account clicks "checkout" in the shopping cart
User clicks "Login"
User can check out faster with saved payment and shipping information upon logging in
