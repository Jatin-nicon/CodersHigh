# Questions from "The Code Book" by Simon Singh

## Question 1 — The Secret Message

Imagine you are a messenger working for a group that wants to assassinate Queen Elizabeth I. You need to send your instructions to another conspirator.

The biggest problem is that the guards may intercept and inspect your message. You need a method where, even if the guards find the message, they do not realize that a secret message exists.

What method would you use to send the message, and how would you hide it so that the guards are unlikely to discover it? Explain your method.

<details>
<summary><b>Answer: Invisible Ink (Steganography)</b></summary>

**Details:** I would use a classic steganographic method: invisible ink. First, I would write a completely ordinary, boring letter to an associate discussing mundane matters like the weather, trade, or family health. Then, in the spaces between the lines of this innocent letter, I would write the true, secret instructions using milk or lemon juice. 

When the liquid dries, the paper appears completely blank in those areas. If the guards intercept and inspect the letter, they will read the decoy message, find it harmless, and let it pass. The receiving conspirator, knowing the secret, would gently hold the paper near a heat source like a candle flame. The heat causes the organic matter in the invisible ink to oxidize and turn brown, revealing the hidden assassination instructions without the guards ever knowing a secret message existed.
</details>

---

## Question 2 — Steganography or Cryptography?

You need to secretly send a message to another person. You write the message on a wooden block and cover it with candle wax, so that anyone inspecting the block sees only an ordinary piece of wood covered in wax.

What is this technique an example of?

A. Cryptography | B. Steganography | C. Transposition | D. Substitution

<details>
<summary><b>Answer: B. Steganography</b></summary>

**Details:** Steganography is the art and science of hiding the very existence of a message. By covering the inscribed wooden block with wax, the object looks entirely innocent to any interceptor. Because the primary goal is to conceal the fact that a message even exists (rather than scrambling its meaning), this is a prime example of steganography.
</details>

---

## Question 3 — What Is This Technique Called?

You have an important message that you do not want to encrypt or alter in any way. Instead, you want to hide the message so that nobody realizes that a secret message exists.

For example, you could:
* write it somewhere on the body and cover it with clothing,
* write it on a person's scalp and wait for the hair to grow back, or
* hide it beneath a layer of wax.

What is this technique called?

A. Cryptography | B. Transposition | C. Steganography | D. Substitution

<details>
<summary><b>Answer: C. Steganography</b></summary>

**Details:** All the examples provided—hiding a message under clothing, under grown hair, or beneath a layer of wax—are physical methods of concealing the message's existence. In contrast to cryptography, which hides the *meaning* of a visible message, steganography hides the *presence* of the message entirely.
</details>

---

## Question 4 — Two Branches of Cryptography

You have learned that cryptography hides the meaning of a message by scrambling it according to a secret system. The book explains that cryptography can be divided into two main branches.

What are the two branches of cryptography?

A. Steganography and cryptography | B. Transposition and substitution | C. Encryption and decryption | D. Rail fence and scytale

<details>
<summary><b>Answer: B. Transposition and substitution</b></summary>

**Details:** Cryptography (the practice of hiding the meaning of a message) is fundamentally divided into two branches: 
1. **Transposition:** rearranging the existing letters of the message into a new, scrambled order.
2. **Substitution:** replacing the letters of the message with entirely different letters, numbers, or symbols.
</details>

---

## Question 5 — The Message Is Shuffled

The hiding method you used earlier is unreliable. This time, you decide not to hide the message physically. Instead, you take the original message:

“THY SECRET IS THY PRISONER; IF THOU LET IT GO, THOU ART A PRISONER TO IT”

and rearrange its letters according to a predetermined pattern, producing a sequence that appears meaningless:

TYERTSHPIOEITOLTTOHURARSNROTHSCEITYRSNRFHUEIGTOATPIOETI

What is this technique called?

A. Substitution | B. Transposition

<details>
<summary><b>Answer: B. Transposition</b></summary>

**Details:** Because the original letters of the message have not been replaced with different symbols, but rather shuffled and rearranged into a new order according to a specific pattern, this is a classic transposition cipher.
</details>