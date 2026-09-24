# Encode and Decode Strings

LeetCode 271 - Encode and Decode Strings

## Problem Statement

Design an algorithm to encode a list of strings into a single string and decode the encoded string back into the original list of strings.

The encoding should preserve the exact content and order of all strings.

## Approach

To encode the strings, store the length of each string followed by a special delimiter `#` and then the actual string.

For example:

["hello", "world"]

can be encoded as:

5#hello5#world

During decoding, first find the `#` character to determine the length of the string. Then use that length to extract the exact number of characters from the encoded string.

This allows strings containing spaces, numbers, or special characters to be decoded correctly.

## Algorithm

### Encoding
1. Create an empty result string.
2. Traverse each string in the list.
3. Add its length followed by `#`.
4. Add the string itself.
5. Return the encoded string.

### Decoding
1. Create an empty result list.
2. Start from the first character.
3. Find the `#` delimiter.
4. Convert the characters before `#` into the string length.
5. Extract that many characters.
6. Add the extracted string to the result.
7. Continue until the entire encoded string is processed.

## Example

Input:
["hello", "world"]

Encoded:
5#hello5#world

Decoded:
["hello", "world"]

## Complexity

- Time Complexity: O(n)
- Space Complexity: O(n)

## Author

T. Nandhini
