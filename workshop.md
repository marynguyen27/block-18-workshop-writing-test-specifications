# Unit Tests

## multiplication

### A function called "multiplication" that returns the product of the two input numbers.

- Expect multiplication(2,4) to be a number
- Expect multiplication(2,4) to be equal to 8
- Expect multiplication("z",4) to be an error

## concat Odds

### A function called "concatOdds" takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both of the arrays.

- Expect concatOdds([3,2,1], [2,4,5]) to return only the odd numbers 3, 1, 5
- Expect concatOdds([], [2,4,5]) to return only 5 // in case of empty array
- Expect concatOdds([2,4], [2,4,6]) to return [] // empty if there are no odd numbers
- Expect concatOdds([1,3,3], [1,3,5]) to return 1,3,3,1,3,5 // account for duplicates
- Expect concatOdds([happy], [sad]) to return an error // not an integer input

# Functional Tests

- When a user views their cart and clicks "check out," they should be checked for if they are logged in or not already
- When a user clicks on "check out," they should be prompted with a question of if they want to create an account, log in, or continue as a guest
- When a user clicks on "Create an account" they are taken to the next page where they can input their email address and desired password to create an account, then they are redirected back to the cart to continue check out
- When a user clicks on "log in" they are taken to a log in screen to input their credentials, then they are redirected back to the cart to continue check out
- When a user clicks on "continue as a guest" they continue the check out flow
- When a user goes to check out and the cart is empty, they should see a message letting them know there is nothing to check out, and that they should add items to the cart before they can check out
- When a user completed the check out process as a guest, they are then prompted to create an account after the fact at which point they can input a desired password which will save their information from the recently-completed purchase
- If the edge case of the network connectivity is lost during the check out process, revert to saved cart state
