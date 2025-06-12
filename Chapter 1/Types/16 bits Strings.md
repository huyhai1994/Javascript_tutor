“16 bits” simply means 16 binary digits (each digit is a 0 or a 1). A group of 16 such bits can represent 2¹⁶ (65 536) distinct values. In more familiar terms:

* **Bits and bytes**:

  * 1 bit = one binary digit (0 or 1)
  * 8 bits = 1 byte
  * 16 bits = 2 bytes

* **Why 16 bits per character?**
  JavaScript strings are stored in UTF-16, meaning each “code unit” (often one character) uses 16 bits of memory. That lets you encode up to 65 536 different code points in a single unit.

So when you hear “16 bits,” think “a bucket of 16 binary switches,” which can be in any of 65 536 configurations.
