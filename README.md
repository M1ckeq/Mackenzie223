/**
 * Checks if a three-digit number is a palindrome.
 *
 * @param {number} number - The three-digit number to check.
 * @returns {boolean} True if the number is a palindrome, false otherwise.
 * @throws {Error} Throws an error if the number is not a three-digit number.
 */
function isPalindrome(number) {
    if (number < 100 || number > 999) {
        throw new Error("Number should be a three-digit number.");
    }
 
    const digits = String(number).split("");
    return digits[0] === digits[2];
}
 
// Usage Example
 
try {
    const userInput = parseInt(prompt("Enter a three-digit number:"));
    const result = isPalindrome(userInput);
    console.log(result ? 1 : 0);
} catch (error) {
    console.error(error.message);
}
