# crypto
Cryptography
## Cryptography
Cryptography, or cryptology (from Ancient Greek: κρυπτός, romanized: kryptós "hidden, secret"; and γράφειν graphein, "to write", or -λογία -logia, "study", respectively[1]), is the practice and study of techniques for secure communication in the presence of third parties called adversaries.[2] More generally, cryptography is about constructing and analyzing protocols that prevent third parties or the public from reading private messages;[3] various aspects in information security such as data confidentiality, data integrity, authentication, and non-repudiation[4] are central to modern cryptography. Modern cryptography exists at the intersection of the disciplines of mathematics, computer science, electrical engineering, communication science, and physics. Applications of cryptography include electronic commerce, chip-based payment cards, digital currencies, computer passwords, and military communications.

Cryptography prior to the modern age was effectively synonymous with encryption, the conversion of information from a readable state to apparent nonsense. The originator of an encrypted message shares the decoding technique only with intended recipients to preclude access from adversaries. The cryptography literature often uses the names Alice ("A") for the sender, Bob ("B") for the intended recipient, and Eve ("eavesdropper") for the adversary.[5] Since the development of rotor cipher machines in World War I and the advent of computers in World War II, the methods used to carry out cryptology have become increasingly complex and its application more widespread.

Modern cryptography is heavily based on mathematical theory and computer science practice; cryptographic algorithms are designed around computational hardness assumptions, making such algorithms hard to break in practice by any adversary. It is theoretically possible to break such a system, but it is infeasible to do so by any known practical means. These schemes are therefore termed computationally secure; theoretical advances, e.g., improvements in integer factorization algorithms, and faster computing technology require these solutions to be continually adapted. There exist information-theoretically secure schemes that provably cannot be broken even with unlimited computing power—an example is the one-time pad—but these schemes are more difficult to use in practice than the best theoretically breakable but computationally secure mechanisms.

The growth of cryptographic technology has raised a number of legal issues in the information age. Cryptography's potential for use as a tool for espionage and sedition has led many governments to classify it as a weapon and to limit or even prohibit its use and export.[6] In some jurisdictions where the use of cryptography is legal, laws permit investigators to compel the disclosure of encryption keys for documents relevant to an investigation.[7][8] Cryptography also plays a major role in digital rights management and copyright infringement of digital media.[9]


Contents
1	Terminology
2	History of cryptography and cryptanalysis
2.1	Classic cryptography
2.2	Computer era
2.3	Advent of modern cryptography
3	Modern cryptography
3.1	Symmetric-key cryptography
3.2	Public-key cryptography
3.3	Cryptanalysis
3.4	Cryptographic primitives
3.5	Cryptosystems
4	Legal issues
4.1	Prohibitions
4.2	Export controls
4.3	NSA involvement
4.4	Digital rights management
4.5	Forced disclosure of encryption keys
5	See also
6	References
7	Further reading
8	External links
Terminology
diagram showing shift three alphabetic cypher D becomes A and E becomes B
Alphabet shift ciphers are believed to have been used by Julius Caesar over 2,000 years ago.[5] This is an example with k = 3. In other words, the letters in the alphabet are shifted three in one direction to encrypt and three in the other direction to decrypt.
The first use of the term cryptograph (as opposed to cryptogram) dates back to the 19th century—originating from The Gold-Bug, a novel by Edgar Allan Poe.[10][11][broken footnote]

Until modern times, cryptography referred almost exclusively to encryption, which is the process of converting ordinary information (called plaintext) into unintelligible form (called ciphertext).[12] Decryption is the reverse, in other words, moving from the unintelligible ciphertext back to plaintext. A cipher (or cypher) is a pair of algorithms that create the encryption and the reversing decryption. The detailed operation of a cipher is controlled both by the algorithm and in each instance by a "key". The key is a secret (ideally known only to the communicants), usually a short string of characters, which is needed to decrypt the ciphertext. Formally, a "cryptosystem" is the ordered list of elements of finite possible plaintexts, finite possible cyphertexts, finite possible keys, and the encryption and decryption algorithms which correspond to each key. Keys are important both formally and in actual practice, as ciphers without variable keys can be trivially broken with only the knowledge of the cipher used and are therefore useless (or even counter-productive) for most purposes.

Historically, ciphers were often used directly for encryption or decryption without additional procedures such as authentication or integrity checks. There are two kinds of cryptosystems: symmetric and asymmetric. In symmetric systems the same key (the secret key) is used to encrypt and decrypt a message. Data manipulation in symmetric systems is faster than asymmetric systems as they generally use shorter key lengths. Asymmetric systems use a public key to encrypt a message and a private key to decrypt it. Use of asymmetric systems enhances the security of communication.[13] Examples of asymmetric systems include RSA (Rivest–Shamir–Adleman), and ECC (Elliptic Curve Cryptography). Symmetric models include the commonly used AES (Advanced Encryption Standard) which replaced the older DES (Data Encryption Standard).[14]

In colloquial use, the term "code" is often used to mean any method of encryption or concealment of meaning. However, in cryptography, code has a more specific meaning: the replacement of a unit of plaintext (i.e., a meaningful word or phrase) with a code word (for example, "wallaby" replaces "attack at dawn").

Cryptanalysis is the term used for the study of methods for obtaining the meaning of encrypted information without access to the key normally required to do so; i.e., it is the study of how to crack encryption algorithms or their implementations.

Some use the terms cryptography and cryptology interchangeably in English, while others (including US military practice generally) use cryptography to refer specifically to the use and practice of cryptographic techniques and cryptology to refer to the combined study of cryptography and cryptanalysis.[15][16] English is more flexible than several other languages in which cryptology (done by cryptologists) is always used in the second sense above. RFC 2828 advises that steganography is sometimes included in cryptology.[17]

The study of characteristics of languages that have some application in cryptography or cryptology (e.g. frequency data, letter combinations, universal patterns, etc.) is called cryptolinguistics.

History of cryptography and cryptanalysis
Main article: History of cryptography
Before the modern era, cryptography focused on message confidentiality (i.e., encryption)—conversion of messages from a comprehensible form into an incomprehensible one and back again at the other end, rendering it unreadable by interceptors or eavesdroppers without secret knowledge (namely the key needed for decryption of that message). Encryption attempted to ensure secrecy in communications, such as those of spies, military leaders, and diplomats. In recent decades, the field has expanded beyond confidentiality concerns to include techniques for message integrity checking, sender/receiver identity authentication, digital signatures, interactive proofs and secure computation, among others.

Classic cryptography
Skytala stick with strip of paper wound around in spiral
Reconstructed ancient Greek scytale, an early cipher device
The main classical cipher types are transposition ciphers, which rearrange the order of letters in a message (e.g., 'hello world' becomes 'ehlol owrdl' in a trivially simple rearrangement scheme), and substitution ciphers, which systematically replace letters or groups of letters with other letters or groups of letters (e.g., 'fly at once' becomes 'gmz bu podf' by replacing each letter with the one following it in the Latin alphabet). Simple versions of either have never offered much confidentiality from enterprising opponents. An early substitution cipher was the Caesar cipher, in which each letter in the plaintext was replaced by a letter some fixed number of positions further down the alphabet. Suetonius reports that Julius Caesar used it with a shift of three to communicate with his generals. Atbash is an example of an early Hebrew cipher. The earliest known use of cryptography is some carved ciphertext on stone in Egypt (ca 1900 BCE), but this may have been done for the amusement of literate observers rather than as a way of concealing information.

The Greeks of Classical times are said to have known of ciphers (e.g., the scytale transposition cipher claimed to have been used by the Spartan military).[18] Steganography (i.e., hiding even the existence of a message so as to keep it confidential) was also first developed in ancient times. An early example, from Herodotus, was a message tattooed on a slave's shaved head and concealed under the regrown hair.[12] More modern examples of steganography include the use of invisible ink, microdots, and digital watermarks to conceal information.

In India, the 2000-year-old Kamasutra of Vātsyāyana speaks of two different kinds of ciphers called Kautiliyam and Mulavediya. In the Kautiliyam, the cipher letter substitutions are based on phonetic relations, such as vowels becoming consonants. In the Mulavediya, the cipher alphabet consists of pairing letters and using the reciprocal ones.[12]

In Sassanid Persia, there were two secret scripts, according to the Muslim author Ibn al-Nadim: the šāh-dabīrīya (literally "King's script") which was used for official correspondence, and the rāz-saharīya which was used to communicate secret messages with other countries.[19]

David Kahn notes in The Codebreakers that modern cryptology originated among the Arabs, the first people to systematically document cryptanalytic methods.[20] Al-Khalil (717–786) wrote the Book of Cryptographic Messages, which contains the first use of permutations and combinations to list all possible Arabic words with and without vowels.[21]

Arabic text of a book by Al-Kindi
First page of a book by Al-Kindi which discusses encryption of messages
Ciphertexts produced by a classical cipher (and some modern ciphers) will reveal statistical information about the plaintext, and that information can often be used to break the cipher. After the discovery of frequency analysis, by the Arab mathematician and polymath Al-Kindi (also known as Alkindus) in the 9th century,[22][23][24] nearly all such ciphers could be broken by an informed attacker. Such classical ciphers still enjoy popularity today, though mostly as puzzles. Al-Kindi wrote a book on cryptography entitled Risalah fi Istikhraj al-Mu'amma (Manuscript for the Deciphering Cryptographic Messages), which described the first known use of frequency analysis and cryptanalysis techniques.[22][25] An important contribution of Ibn Adlan (1187–1268) was on sample size for use of frequency analysis.[21]

book sized metal machine with large dial left page and nineteen small dials right page
16th-century book-shaped French cipher machine, with arms of Henri II of France
manuscript from Gabriel de Luetz d'Aramon in bound volume
Enciphered letter from Gabriel de Luetz d'Aramon, French Ambassador to the Ottoman Empire, after 1546, with partial decipherment
Language letter frequencies may offer little help for some extended historical encryption techniques such as homophonic cipher that tend to flatten the frequency distribution. For those ciphers, language letter group (or n-gram) frequencies may provide an attack.

Essentially all ciphers remained vulnerable to cryptanalysis using the frequency analysis technique until the development of the polyalphabetic cipher. While it was known to Al-Kindi to some extent,[25][26] it was first clearly described in the work of Al-Qalqashandi (1355–1418), based on the earlier work of Ibn al-Durayhim (1312–1359), describing a polyalphabetic cipher in which each plaintext letter is assigned more than one substitute.[27] It was later also described by Leon Battista Alberti around the year 1467, though there is some indication that Alberti's method was to use different ciphers (i.e., substitution alphabets) for various parts of a message (perhaps for each successive plaintext letter at the limit). He also invented what was probably the first automatic cipher device, a wheel which implemented a partial realization of his invention. In the Vigenère cipher, a polyalphabetic cipher, encryption uses a key word, which controls letter substitution depending on which letter of the key word is used. In the mid-19th century Charles Babbage showed that the Vigenère cipher was vulnerable to Kasiski examination, but this was first published about ten years later by Friedrich Kasiski.[28]

Although frequency analysis can be a powerful and general technique against many ciphers, encryption has still often been effective in practice, as many a would-be cryptanalyst was unaware of the technique. Breaking a message without using frequency analysis essentially required knowledge of the cipher used and perhaps of the key involved, thus making espionage, bribery, burglary, defection, etc., more attractive approaches to the cryptanalytically uninformed. It was finally explicitly recognized in the 19th century that secrecy of a cipher's algorithm is not a sensible nor practical safeguard of message security; in fact, it was further realized that any adequate cryptographic scheme (including ciphers) should remain secure even if the adversary fully understands the cipher algorithm itself. Security of the key used should alone be sufficient for a good cipher to maintain confidentiality under an attack. This fundamental principle was first explicitly stated in 1883 by Auguste Kerckhoffs and is generally called Kerckhoffs's Principle; alternatively and more bluntly, it was restated by Claude Shannon, the inventor of information theory and the fundamentals of theoretical cryptography, as Shannon's Maxim—'the enemy knows the system'.

Different physical devices and aids have been used to assist with ciphers. One of the earliest may have been the scytale of ancient Greece, a rod supposedly used by the Spartans as an aid for a transposition cipher. In medieval times, other aids were invented such as the cipher grille, which was also used for a kind of steganography. With the invention of polyalphabetic ciphers came more sophisticated aids such as Alberti's own cipher disk, Johannes Trithemius' tabula recta scheme, and Thomas Jefferson's wheel cypher (not publicly known, and reinvented independently by Bazeries around 1900). Many mechanical encryption/decryption devices were invented early in the 20th century, and several patented, among them rotor machines—famously including the Enigma machine used by the German government and military from the late 1920s and during World War II.[29] The ciphers implemented by better quality examples of these machine designs brought about a substantial increase in cryptanalytic difficulty after WWI.[30]

Computer era
Prior to the early 20th century, cryptography was mainly concerned with linguistic and lexicographic patterns. Since then the emphasis has shifted, and cryptography now makes extensive use of mathematics, including aspects of information theory, computational complexity, statistics, combinatorics, abstract algebra, number theory, and finite mathematics generally. Cryptography is also a branch of engineering, but an unusual one since it deals with active, intelligent, and malevolent opposition; other kinds of engineering (e.g., civil or chemical engineering) need deal only with neutral natural forces. There is also active research examining the relationship between cryptographic problems and quantum physics.

Just as the development of digital computers and electronics helped in cryptanalysis, it made possible much more complex ciphers. Furthermore, computers allowed for the encryption of any kind of data representable in any binary format, unlike classical ciphers which only encrypted written language texts; this was new and significant. Computer use has thus supplanted linguistic cryptography, both for cipher design and cryptanalysis. Many computer ciphers can be characterized by their operation on binary bit sequences (sometimes in groups or blocks), unlike classical and mechanical schemes, which generally manipulate traditional characters (i.e., letters and digits) directly. However, computers have also assisted cryptanalysis, which has compensated to some extent for increased cipher complexity. Nonetheless, good modern ciphers have stayed ahead of cryptanalysis; it is typically the case that use of a quality cipher is very efficient (i.e., fast and requiring few resources, such as memory or CPU capability), while breaking it requires an effort many orders of magnitude larger, and vastly larger than that required for any classical cipher, making cryptanalysis so inefficient and impractical as to be effectively impossible.

Advent of modern cryptography
Cryptanalysis of the new mechanical devices proved to be both difficult and laborious. In the United Kingdom, cryptanalytic efforts at Bletchley Park during WWII spurred the development of more efficient means for carrying out repetitious tasks. This culminated in the development of the Colossus, the world's first fully electronic, digital, programmable computer, which assisted in the decryption of ciphers generated by the German Army's Lorenz SZ40/42 machine.

Extensive open academic research into cryptography is relatively recent; it began only in the mid-1970s. In recent times, IBM personnel designed the algorithm that became the Federal (i.e., US) Data Encryption Standard; Whitfield Diffie and Martin Hellman published their key agreement algorithm;[31] and the RSA algorithm was published in Martin Gardner's Scientific American column. Following their work in 1976, it became popular to consider cryptography systems based on mathematical problems that are easy to state but have been found difficult to solve.[32] Since then, cryptography has become a widely used tool in communications, computer networks, and computer security generally. Some modern cryptographic techniques can only keep their keys secret if certain mathematical problems are intractable, such as the integer factorization or the discrete logarithm problems, so there are deep connections with abstract mathematics. There are very few cryptosystems that are proven to be unconditionally secure. The one-time pad is one, and was proven to be so by Claude Shannon. There are a few important algorithms that have been proven secure under certain assumptions. For example, the infeasibility of factoring extremely large integers is the basis for believing that RSA is secure, and some other systems, but even so proof of unbreakability is unavailable since the underlying mathematical problem remains open. In practice, these are widely used, and are believed unbreakable in practice by most competent observers. There are systems similar to RSA, such as one by Michael O. Rabin that are provably secure provided factoring n = pq is impossible; it is quite unusable in practice. The discrete logarithm problem is the basis for believing some other cryptosystems are secure, and again, there are related, less practical systems that are provably secure relative to the solvability or insolvability discrete log problem.[33]

As well as being aware of cryptographic history, cryptographic algorithm and system designers must also sensibly consider probable future developments while working on their designs. For instance, continuous improvements in computer processing power have increased the scope of brute-force attacks, so when specifying key lengths, the required key lengths are similarly advancing.[34] The potential effects of quantum computing are already being considered by some cryptographic system designers developing post-quantum cryptography; the announced imminence of small implementations of these machines may be making the need for preemptive caution rather more than merely speculative.[4]

Modern cryptography
Symmetric-key cryptography
Main article: Symmetric-key algorithm
diagram showing encrypt with a key and decrypt process
Symmetric-key cryptography, where a single key is used for encryption and decryption
Symmetric-key cryptography refers to encryption methods in which both the sender and receiver share the same key (or, less commonly, in which their keys are different, but related in an easily computable way). This was the only kind of encryption publicly known until June 1976.[31]

logic diagram showing International Data Encryption Algorithm cypher process
One round (out of 8.5) of the IDEA cipher, used in most versions of PGP and OpenPGP compatible software for time-efficient encryption of messages
Symmetric key ciphers are implemented as either block ciphers or stream ciphers. A block cipher enciphers input in blocks of plaintext as opposed to individual characters, the input form used by a stream cipher.

The Data Encryption Standard (DES) and the Advanced Encryption Standard (AES) are block cipher designs that have been designated cryptography standards by the US government (though DES's designation was finally withdrawn after the AES was adopted).[35] Despite its deprecation as an official standard, DES (especially its still-approved and much more secure triple-DES variant) remains quite popular; it is used across a wide range of applications, from ATM encryption[36] to e-mail privacy[37] and secure remote access.[38] Many other block ciphers have been designed and released, with considerable variation in quality. Many, even some designed by capable practitioners, have been thoroughly broken, such as FEAL.[4][39]

Stream ciphers, in contrast to the 'block' type, create an arbitrarily long stream of key material, which is combined with the plaintext bit-by-bit or character-by-character, somewhat like the one-time pad. In a stream cipher, the output stream is created based on a hidden internal state that changes as the cipher operates. That internal state is initially set up using the secret key material. RC4 is a widely used stream cipher.[4] Block ciphers can be used as stream ciphers.

Cryptographic hash functions are a third type of cryptographic algorithm. They take a message of any length as input, and output a short, fixed length hash, which can be used in (for example) a digital signature. For good hash functions, an attacker cannot find two messages that produce the same hash. MD4 is a long-used hash function that is now broken; MD5, a strengthened variant of MD4, is also widely used but broken in practice. The US National Security Agency developed the Secure Hash Algorithm series of MD5-like hash functions: SHA-0 was a flawed algorithm that the agency withdrew; SHA-1 is widely deployed and more secure than MD5, but cryptanalysts have identified attacks against it; the SHA-2 family improves on SHA-1, but is vulnerable to clashes as of 2011; and the US standards authority thought it "prudent" from a security perspective to develop a new standard to "significantly improve the robustness of NIST's overall hash algorithm toolkit."[40] Thus, a hash function design competition was meant to select a new U.S. national standard, to be called SHA-3, by 2012. The competition ended on October 2, 2012 when the NIST announced that Keccak would be the new SHA-3 hash algorithm.[41] Unlike block and stream ciphers that are invertible, cryptographic hash functions produce a hashed output that cannot be used to retrieve the original input data. Cryptographic hash functions are used to verify the authenticity of data retrieved from an untrusted source or to add a layer of security.

Message authentication codes (MACs) are much like cryptographic hash functions, except that a secret key can be used to authenticate the hash value upon receipt;[4] this additional complication blocks an attack scheme against bare digest algorithms, and so has been thought worth the effort.

Public-key cryptography
Main article: Public-key cryptography
diagram of Public-key cryptography showing public key and private key
Public-key cryptography, where different keys are used for encryption and decryption.
padlock icon in the internet browser line next to the url
Padlock icon from the Firefox Web browser, which indicates that TLS, a public-key cryptography system, is in use.
Symmetric-key cryptosystems use the same key for encryption and decryption of a message, although a message or group of messages can have a different key than others. A significant disadvantage of symmetric ciphers is the key management necessary to use them securely. Each distinct pair of communicating parties must, ideally, share a different key, and perhaps for each ciphertext exchanged as well. The number of keys required increases as the square of the number of network members, which very quickly requires complex key management schemes to keep them all consistent and secret.

headshots of Whitfield Diffie and Martin Hellman
Whitfield Diffie and Martin Hellman, authors of the first published paper on public-key cryptography.
In a groundbreaking 1976 paper, Whitfield Diffie and Martin Hellman proposed the notion of public-key (also, more generally, called asymmetric key) cryptography in which two different but mathematically related keys are used—a public key and a private key.[42] A public key system is so constructed that calculation of one key (the 'private key') is computationally infeasible from the other (the 'public key'), even though they are necessarily related. Instead, both keys are generated secretly, as an interrelated pair.[43] The historian David Kahn described public-key cryptography as "the most revolutionary new concept in the field since polyalphabetic substitution emerged in the Renaissance".[44]

In public-key cryptosystems, the public key may be freely distributed, while its paired private key must remain secret. In a public-key encryption system, the public key is used for encryption, while the private or secret key is used for decryption. While Diffie and Hellman could not find such a system, they showed that public-key cryptography was indeed possible by presenting the Diffie–Hellman key exchange protocol, a solution that is now widely used in secure communications to allow two parties to secretly agree on a shared encryption key.[31] The X.509 standard defines the most commonly used format for public key certificates.[45]

Diffie and Hellman's publication sparked widespread academic efforts in finding a practical public-key encryption system. This race was finally won in 1978 by Ronald Rivest, Adi Shamir, and Len Adleman, whose solution has since become known as the RSA algorithm.[46]

The Diffie–Hellman and RSA algorithms, in addition to being the first publicly known examples of high quality public-key algorithms, have been among the most widely used. Other asymmetric-key algorithms include the Cramer–Shoup cryptosystem, ElGamal encryption, and various elliptic curve techniques.[citation needed]

A document published in 1997 by the Government Communications Headquarters (GCHQ), a British intelligence organization, revealed that cryptographers at GCHQ had anticipated several academic developments.[47] Reportedly, around 1970, James H. Ellis had conceived the principles of asymmetric key cryptography. In 1973, Clifford Cocks invented a solution that very similar in design rationale to RSA.[47][48] And in 1974, Malcolm J. Williamson is claimed to have developed the Diffie–Hellman key exchange.[49]


In this example the message is only signed and not encrypted. 1) Alice signs a message with her private key. 2) Bob can verify that Alice sent the message and that the message has not been modified.
Public-key cryptography is also used for implementing digital signature schemes. A digital signature is reminiscent of an ordinary signature; they both have the characteristic of being easy for a user to produce, but difficult for anyone else to forge. Digital signatures can also be permanently tied to the content of the message being signed; they cannot then be 'moved' from one document to another, for any attempt will be detectable. In digital signature schemes, there are two algorithms: one for signing, in which a secret key is used to process the message (or a hash of the message, or both), and one for verification, in which the matching public key is used with the message to check the validity of the signature. RSA and DSA are two of the most popular digital signature schemes. Digital signatures are central to the operation of public key infrastructures and many network security schemes (e.g., SSL/TLS, many VPNs, etc.).[39]

Public-key algorithms are most often based on the computational complexity of "hard" problems, often from number theory. For example, the hardness of RSA is related to the integer factorization problem, while Diffie–Hellman and DSA are related to the discrete logarithm problem. The security of elliptic curve cryptography is based on number theoretic problems involving elliptic curves. Because of the difficulty of the underlying problems, most public-key algorithms involve operations such as modular multiplication and exponentiation, which are much more computationally expensive than the techniques used in most block ciphers, especially with typical key sizes. As a result, public-key cryptosystems are commonly hybrid cryptosystems, in which a fast high-quality symmetric-key encryption algorithm is used for the message itself, while the relevant symmetric key is sent with the message, but encrypted using a public-key algorithm. Similarly, hybrid signature schemes are often used, in which a cryptographic hash function is computed, and only the resulting hash is digitally signed.[4]

Cryptanalysis
Main article: Cryptanalysis
Enigma machine typewriter keypad over many rotors in a wood box
Variants of the Enigma machine, used by Germany's military and civil authorities from the late 1920s through World War II, implemented a complex electro-mechanical polyalphabetic cipher. Breaking and reading of the Enigma cipher at Poland's Cipher Bureau, for 7 years before the war, and subsequent decryption at Bletchley Park, was important to Allied victory.[12]
The goal of cryptanalysis is to find some weakness or insecurity in a cryptographic scheme, thus permitting its subversion or evasion.

It is a common misconception that every encryption method can be broken. In connection with his WWII work at Bell Labs, Claude Shannon proved that the one-time pad cipher is unbreakable, provided the key material is truly random, never reused, kept secret from all possible attackers, and of equal or greater length than the message.[50] Most ciphers, apart from the one-time pad, can be broken with enough computational effort by brute force attack, but the amount of effort needed may be exponentially dependent on the key size, as compared to the effort needed to make use of the cipher. In such cases, effective security could be achieved if it is proven that the effort required (i.e., "work factor", in Shannon's terms) is beyond the ability of any adversary. This means it must be shown that no efficient method (as opposed to the time-consuming brute force method) can be found to break the cipher. Since no such proof has been found to date, the one-time-pad remains the only theoretically unbreakable cipher.

There are a wide variety of cryptanalytic attacks, and they can be classified in any of several ways. A common distinction turns on what Eve (an attacker) knows and what capabilities are available. In a ciphertext-only attack, Eve has access only to the ciphertext (good modern cryptosystems are usually effectively immune to ciphertext-only attacks). In a known-plaintext attack, Eve has access to a ciphertext and its corresponding plaintext (or to many such pairs). In a chosen-plaintext attack, Eve may choose a plaintext and learn its corresponding ciphertext (perhaps many times); an example is gardening, used by the British during WWII. In a chosen-ciphertext attack, Eve may be able to choose ciphertexts and learn their corresponding plaintexts.[4] Finally in a man-in-the-middle attack Eve gets in between Alice (the sender) and Bob (the recipient), accesses and modifies the traffic and then forwards it to the recipient.[51] Also important, often overwhelmingly so, are mistakes (generally in the design or use of one of the protocols involved).

Kaiserschloss Kryptologen monument numbers on stele
Poznań monument (center) to Polish cryptanalysts whose breaking of Germany's Enigma machine ciphers, beginning in 1932, altered the course of World War II
Cryptanalysis of symmetric-key ciphers typically involves looking for attacks against the block ciphers or stream ciphers that are more efficient than any attack that could be against a perfect cipher. For example, a simple brute force attack against DES requires one known plaintext and 255 decryptions, trying approximately half of the possible keys, to reach a point at which chances are better than even that the key sought will have been found. But this may not be enough assurance; a linear cryptanalysis attack against DES requires 243 known plaintexts (with their corresponding ciphertexts) and approximately 243 DES operations.[52] This is a considerable improvement over brute force attacks.

Public-key algorithms are based on the computational difficulty of various problems. The most famous of these are the difficulty of integer factorization of semiprimes and the difficulty of calculating discrete logarithms, both of which are not yet proven to be solvable in polynomial time using only a classical Turing-complete computer. Much public-key cryptanalysis concerns designing algorithms in P that can solve these problems, or using other technologies, such as quantum computers. For instance, the best known algorithms for solving the elliptic curve-based version of discrete logarithm are much more time-consuming than the best known algorithms for factoring, at least for problems of more or less equivalent size. Thus, other things being equal, to achieve an equivalent strength of attack resistance, factoring-based encryption techniques must use larger keys than elliptic curve techniques. For this reason, public-key cryptosystems based on elliptic curves have become popular since their invention in the mid-1990s.

While pure cryptanalysis uses weaknesses in the algorithms themselves, other attacks on cryptosystems are based on actual use of the algorithms in real devices, and are called side-channel attacks. If a cryptanalyst has access to, for example, the amount of time the device took to encrypt a number of plaintexts or report an error in a password or PIN character, he may be able to use a timing attack to break a cipher that is otherwise resistant to analysis. An attacker might also study the pattern and length of messages to derive valuable information; this is known as traffic analysis[53] and can be quite useful to an alert adversary. Poor administration of a cryptosystem, such as permitting too short keys, will make any system vulnerable, regardless of other virtues. Social engineering and other attacks against humans (e.g., bribery, extortion, blackmail, espionage, torture, ...) are usually employed due to being more cost-effective and feasible to perform in a reasonable amount of time compared to pure cryptanalysis by a high margin.

Cryptographic primitives
Much of the theoretical work in cryptography concerns cryptographic primitives—algorithms with basic cryptographic properties—and their relationship to other cryptographic problems. More complicated cryptographic tools are then built from these basic primitives. These primitives provide fundamental properties, which are used to develop more complex tools called cryptosystems or cryptographic protocols, which guarantee one or more high-level security properties. Note however, that the distinction between cryptographic primitives and cryptosystems, is quite arbitrary; for example, the RSA algorithm is sometimes considered a cryptosystem, and sometimes a primitive. Typical examples of cryptographic primitives include pseudorandom functions, one-way functions, etc.

Cryptosystems
One or more cryptographic primitives are often used to develop a more complex algorithm, called a cryptographic system, or cryptosystem. Cryptosystems (e.g., El-Gamal encryption) are designed to provide particular functionality (e.g., public key encryption) while guaranteeing certain security properties (e.g., chosen-plaintext attack (CPA) security in the random oracle model). Cryptosystems use the properties of the underlying cryptographic primitives to support the system's security properties. As the distinction between primitives and cryptosystems is somewhat arbitrary, a sophisticated cryptosystem can be derived from a combination of several more primitive cryptosystems. In many cases, the cryptosystem's structure involves back and forth communication among two or more parties in space (e.g., between the sender of a secure message and its receiver) or across time (e.g., cryptographically protected backup data). Such cryptosystems are sometimes called cryptographic protocols.

Some widely known cryptosystems include RSA encryption, Schnorr signature, El-Gamal encryption, PGP, etc. More complex cryptosystems include electronic cash[54] systems, signcryption systems, etc. Some more 'theoretical'[clarification needed] cryptosystems include interactive proof systems,[55] (like zero-knowledge proofs),[56] systems for secret sharing,[57][58] etc.

Legal issues
See also: Cryptography laws in different nations
Prohibitions
Cryptography has long been of interest to intelligence gathering and law enforcement agencies.[8] Secret communications may be criminal or even treasonous[citation needed]. Because of its facilitation of privacy, and the diminution of privacy attendant on its prohibition, cryptography is also of considerable interest to civil rights supporters. Accordingly, there has been a history of controversial legal issues surrounding cryptography, especially since the advent of inexpensive computers has made widespread access to high quality cryptography possible.

In some countries, even the domestic use of cryptography is, or has been, restricted. Until 1999, France significantly restricted the use of cryptography domestically, though it has since relaxed many of these rules. In China and Iran, a license is still required to use cryptography.[6] Many countries have tight restrictions on the use of cryptography. Among the more restrictive are laws in Belarus, Kazakhstan, Mongolia, Pakistan, Singapore, Tunisia, and Vietnam.[59]

In the United States, cryptography is legal for domestic use, but there has been much conflict over legal issues related to cryptography.[8] One particularly important issue has been the export of cryptography and cryptographic software and hardware. Probably because of the importance of cryptanalysis in World War II and an expectation that cryptography would continue to be important for national security, many Western governments have, at some point, strictly regulated export of cryptography. After World War II, it was illegal in the US to sell or distribute encryption technology overseas; in fact, encryption was designated as auxiliary military equipment and put on the United States Munitions List.[60] Until the development of the personal computer, asymmetric key algorithms (i.e., public key techniques), and the Internet, this was not especially problematic. However, as the Internet grew and computers became more widely available, high-quality encryption techniques became well known around the globe.

Export controls
Main article: Export of cryptography
In the 1990s, there were several challenges to US export regulation of cryptography. After the source code for Philip Zimmermann's Pretty Good Privacy (PGP) encryption program found its way onto the Internet in June 1991, a complaint by RSA Security (then called RSA Data Security, Inc.) resulted in a lengthy criminal investigation of Zimmermann by the US Customs Service and the FBI, though no charges were ever filed.[61][62] Daniel J. Bernstein, then a graduate student at UC Berkeley, brought a lawsuit against the US government challenging some aspects of the restrictions based on free speech grounds. The 1995 case Bernstein v. United States ultimately resulted in a 1999 decision that printed source code for cryptographic algorithms and systems was protected as free speech by the United States Constitution.[63]

In 1996, thirty-nine countries signed the Wassenaar Arrangement, an arms control treaty that deals with the export of arms and "dual-use" technologies such as cryptography. The treaty stipulated that the use of cryptography with short key-lengths (56-bit for symmetric encryption, 512-bit for RSA) would no longer be export-controlled.[64] Cryptography exports from the US became less strictly regulated as a consequence of a major relaxation in 2000;[65] there are no longer very many restrictions on key sizes in US-exported mass-market software. Since this relaxation in US export restrictions, and because most personal computers connected to the Internet include US-sourced web browsers such as Firefox or Internet Explorer, almost every Internet user worldwide has potential access to quality cryptography via their browsers (e.g., via Transport Layer Security). The Mozilla Thunderbird and Microsoft Outlook E-mail client programs similarly can transmit and receive emails via TLS, and can send and receive email encrypted with S/MIME. Many Internet users don't realize that their basic application software contains such extensive cryptosystems. These browsers and email programs are so ubiquitous that even governments whose intent is to regulate civilian use of cryptography generally don't find it practical to do much to control distribution or use of cryptography of this quality, so even when such laws are in force, actual enforcement is often effectively impossible.[citation needed]

NSA involvement

NSA headquarters in Fort Meade, Maryland
See also: Clipper chip
Another contentious issue connected to cryptography in the United States is the influence of the National Security Agency on cipher development and policy.[8] The NSA was involved with the design of DES during its development at IBM and its consideration by the National Bureau of Standards as a possible Federal Standard for cryptography.[66] DES was designed to be resistant to differential cryptanalysis,[67] a powerful and general cryptanalytic technique known to the NSA and IBM, that became publicly known only when it was rediscovered in the late 1980s.[68] According to Steven Levy, IBM discovered differential cryptanalysis,[62] but kept the technique secret at the NSA's request. The technique became publicly known only when Biham and Shamir re-discovered and announced it some years later. The entire affair illustrates the difficulty of determining what resources and knowledge an attacker might actually have.

Another instance of the NSA's involvement was the 1993 Clipper chip affair, an encryption microchip intended to be part of the Capstone cryptography-control initiative. Clipper was widely criticized by cryptographers for two reasons. The cipher algorithm (called Skipjack) was then classified (declassified in 1998, long after the Clipper initiative lapsed). The classified cipher caused concerns that the NSA had deliberately made the cipher weak in order to assist its intelligence efforts. The whole initiative was also criticized based on its violation of Kerckhoffs's Principle, as the scheme included a special escrow key held by the government for use by law enforcement (i.e. wiretapping).[62]

Digital rights management
Main article: Digital rights management
Cryptography is central to digital rights management (DRM), a group of techniques for technologically controlling use of copyrighted material, being widely implemented and deployed at the behest of some copyright holders. In 1998, U.S. President Bill Clinton signed the Digital Millennium Copyright Act (DMCA), which criminalized all production, dissemination, and use of certain cryptanalytic techniques and technology (now known or later discovered); specifically, those that could be used to circumvent DRM technological schemes.[69] This had a noticeable impact on the cryptography research community since an argument can be made that any cryptanalytic research violated the DMCA. Similar statutes have since been enacted in several countries and regions, including the implementation in the EU Copyright Directive. Similar restrictions are called for by treaties signed by World Intellectual Property Organization member-states.

The United States Department of Justice and FBI have not enforced the DMCA as rigorously as had been feared by some, but the law, nonetheless, remains a controversial one. Niels Ferguson, a well-respected cryptography researcher, has publicly stated that he will not release some of his research into an Intel security design for fear of prosecution under the DMCA.[70] Cryptologist Bruce Schneier has argued that the DMCA encourages vendor lock-in, while inhibiting actual measures toward cyber-security.[71] Both Alan Cox (longtime Linux kernel developer) and Edward Felten (and some of his students at Princeton) have encountered problems related to the Act. Dmitry Sklyarov was arrested during a visit to the US from Russia, and jailed for five months pending trial for alleged violations of the DMCA arising from work he had done in Russia, where the work was legal. In 2007, the cryptographic keys responsible for Blu-ray and HD DVD content scrambling were discovered and released onto the Internet. In both cases, the Motion Picture Association of America sent out numerous DMCA takedown notices, and there was a massive Internet backlash[9] triggered by the perceived impact of such notices on fair use and free speech.

Forced disclosure of encryption keys
Main article: Key disclosure law
In the United Kingdom, the Regulation of Investigatory Powers Act gives UK police the powers to force suspects to decrypt files or hand over passwords that protect encryption keys. Failure to comply is an offense in its own right, punishable on conviction by a two-year jail sentence or up to five years in cases involving national security.[7] Successful prosecutions have occurred under the Act; the first, in 2009,[72] resulted in a term of 13 months' imprisonment.[73] Similar forced disclosure laws in Australia, Finland, France, and India compel individual suspects under investigation to hand over encryption keys or passwords during a criminal investigation.

In the United States, the federal criminal case of United States v. Fricosu addressed whether a search warrant can compel a person to reveal an encryption passphrase or password.[74] The Electronic Frontier Foundation (EFF) argued that this is a violation of the protection from self-incrimination given by the Fifth Amendment.[75] In 2012, the court ruled that under the All Writs Act, the defendant was required to produce an unencrypted hard drive for the court.[76]

In many jurisdictions, the legal status of forced disclosure remains unclear.

The 2016 FBI–Apple encryption dispute concerns the ability of courts in the United States to compel manufacturers' assistance in unlocking cell phones whose contents are cryptographically protected.

As a potential counter-measure to forced disclosure some cryptographic software supports plausible deniability, where the encrypted data is indistinguishable from unused random data (for example such as that of a drive which has been securely wiped).

See also
Outline of cryptography – Overview of and topical guide to cryptography
List of cryptographers – Wikipedia list article
List of important publications in cryptography – Wikipedia list article
List of multiple discoveries – Wikipedia list article
List of unsolved problems in computer science – Wikipedia list article
Syllabical and Steganographical Table – Eighteenth-century work believed to be the first cryptography chart – first cryptography chart
Comparison of cryptography libraries
Crypto Wars
Encyclopedia of Cryptography and Security – Book by Technische Universiteit Eindhoven
Global surveillance – Mass surveillance across national borders
Information theory – Theory dealing with information
Strong cryptography
World Wide Web Consortium's Web Cryptography API
References
 Liddell, Henry George; Scott, Robert; Jones, Henry Stuart; McKenzie, Roderick (1984). A Greek-English Lexicon. Oxford University Press.
 Rivest, Ronald L. (1990). "Cryptography". In J. Van Leeuwen (ed.). Handbook of Theoretical Computer Science. 1. Elsevier.
 Bellare, Mihir; Rogaway, Phillip (21 September 2005). "Introduction". Introduction to Modern Cryptography. p. 10.
 Menezes, A.J.; van Oorschot, P.C.; Vanstone, S.A. (1997). Handbook of Applied Cryptography. ISBN 978-0-8493-8523-0.
 Biggs, Norman (2008). Codes: An introduction to Information Communication and Cryptography. Springer. p. 171.
 "Overview per country". Crypto Law Survey. February 2013. Retrieved 26 March 2015.
 "UK Data Encryption Disclosure Law Takes Effect". PC World. 1 October 2007. Retrieved 26 March 2015.
 Ranger, Steve (24 March 2015). "The undercover war on your internet secrets: How online surveillance cracked our trust in the web". TechRepublic. Archived from the original on 12 June 2016. Retrieved 12 June 2016.
 Doctorow, Cory (2 May 2007). "Digg users revolt over AACS key". Boing Boing. Retrieved 26 March 2015.
 Whalen, Terence (1994). "The Code for Gold: Edgar Allan Poe and Cryptography". Representations. University of California Press. 46 (46): 35–57. doi:10.2307/2928778. JSTOR 2928778.
 Rosenheim 1997, p. 20
 Kahn, David (1967). The Codebreakers. ISBN 978-0-684-83130-5.
 "An Introduction to Modern Cryptosystems".
 Sharbaf, M.S. (1 November 2011). "Quantum cryptography: An emerging technology in network security". 2011 IEEE International Conference on Technologies for Homeland Security (HST). pp. 13–19. doi:10.1109/THS.2011.6107841. ISBN 978-1-4577-1376-7. S2CID 17915038. Missing or empty |title= (help)
 Oded Goldreich, Foundations of Cryptography, Volume 1: Basic Tools, Cambridge University Press, 2001, ISBN 0-521-79172-3
 "Cryptology (definition)". Merriam-Webster's Collegiate Dictionary (11th ed.). Merriam-Webster. Retrieved 26 March 2015.
 "Internet Security Glossary". Internet Engineering Task Force. May 2000. RFC 2828. Retrieved 26 March 2015.
 I︠A︡shchenko, V.V. (2002). Cryptography: an introduction. AMS Bookstore. p. 6. ISBN 978-0-8218-2986-8.
 electricpulp.com. "CODES – Encyclopaedia Iranica". www.iranicaonline.org.
 Kahn, David (1996). The Codebreakers: The Comprehensive History of Secret Communication from Ancient Times to the Internet. Simon and Schuster. ISBN 9781439103555.
 Broemeling, Lyle D. (1 November 2011). "An Account of Early Statistical Inference in Arab Cryptology". The American Statistician. 65 (4): 255–257. doi:10.1198/tas.2011.10191. S2CID 123537702.
 Singh, Simon (2000). The Code Book. New York: Anchor Books. pp. 14–20. ISBN 978-0-385-49532-5.
 Leaman, Oliver (16 July 2015). The Biographical Encyclopedia of Islamic Philosophy. Bloomsbury Publishing. ISBN 9781472569455. Retrieved 19 March 2018 – via Google Books.
 Al-Jubouri, I. M. N. (19 March 2018). History of Islamic Philosophy: With View of Greek Philosophy and Early History of Islam. Authors On Line Ltd. ISBN 9780755210114. Retrieved 19 March 2018 – via Google Books.
 Al-Kadi, Ibrahim A. (April 1992). "The origins of cryptology: The Arab contributions". Cryptologia. 16 (2): 97–126. doi:10.1080/0161-119291866801.
 Simon Singh, The Code Book, pp. 14–20
 Lennon, Brian (2018). Passwords: Philology, Security, Authentication. Harvard University Press. p. 26. ISBN 9780674985377.
 Schrödel, Tobias (October 2008). "Breaking Short Vigenère Ciphers". Cryptologia. 32 (4): 334–337. doi:10.1080/01611190802336097. S2CID 21812933.
 Hakim, Joy (1995). A History of US: War, Peace and all that Jazz. New York: Oxford University Press. ISBN 978-0-19-509514-2.
 Gannon, James (2001). Stealing Secrets, Telling Lies: How Spies and Codebreakers Helped Shape the Twentieth Century. Washington, D.C.: Brassey's. ISBN 978-1-57488-367-1.
 Diffie, Whitfield; Hellman, Martin (November 1976). "New Directions in Cryptography" (PDF). IEEE Transactions on Information Theory. IT-22 (6): 644–654. CiteSeerX 10.1.1.37.9720. doi:10.1109/tit.1976.1055638.
 Wolfram, Stephen (2002). A New Kind of Science. Wolfram Media, Inc. p. 1089. ISBN 978-1-57955-008-0.
 Cryptography: Theory and Practice, Third Edition (Discrete Mathematics and Its Applications), 2005, by Douglas R. Stinson, Chapman and Hall/CRC
 Blaze, Matt; Diffie, Whitefield; Rivest, Ronald L.; Schneier, Bruce; Shimomura, Tsutomu; Thompson, Eric; Wiener, Michael (January 1996). "Minimal key lengths for symmetric ciphers to provide adequate commercial security". Fortify. Retrieved 26 March 2015.
 "FIPS PUB 197: The official Advanced Encryption Standard" (PDF). Computer Security Resource Center. National Institute of Standards and Technology. Archived from the original (PDF) on 7 April 2015. Retrieved 26 March 2015.
 "NCUA letter to credit unions" (PDF). National Credit Union Administration. July 2004. Retrieved 26 March 2015.
 "Open PGP Message Format". Internet Engineering Task Force. November 1998. RFC 2440. Retrieved 26 March 2015.
 Golen, Pawel (19 July 2002). "SSH". WindowSecurity. Retrieved 26 March 2015.
 Schneier, Bruce (1996). Applied Cryptography (2nd ed.). Wiley. ISBN 978-0-471-11709-4.
 "Notices". Federal Register. 72 (212). 2 November 2007.
"Archived copy" (PDF). Archived from the original on 28 February 2008. Retrieved 27 January 2009.
 "NIST Selects Winner of Secure Hash Algorithm (SHA-3) Competition". Tech Beat. National Institute of Standards and Technology. 2 October 2012. Retrieved 26 March 2015.
 Diffie, Whitfield; Hellman, Martin (8 June 1976). "Multi-user cryptographic techniques". AFIPS Proceedings. 45: 109–112. doi:10.1145/1499799.1499815. S2CID 13210741.
 Ralph Merkle was working on similar ideas at the time and encountered publication delays, and Hellman has suggested that the term used should be Diffie–Hellman–Merkle aysmmetric key cryptography.
 Kahn, David (Fall 1979). "Cryptology Goes Public". Foreign Affairs. 58 (1): 141–159. doi:10.2307/20040343. JSTOR 20040343.
 "Using Client-Certificate based authentication with NGINX on Ubuntu - SSLTrust". SSLTrust. Retrieved 13 June 2019.
 Rivest, Ronald L.; Shamir, A.; Adleman, L. (1978). "A Method for Obtaining Digital Signatures and Public-Key Cryptosystems". Communications of the ACM. 21 (2): 120–126. CiteSeerX 10.1.1.607.2677. doi:10.1145/359340.359342. S2CID 2873616.
"Archived copy" (PDF). Archived from the original (PDF) on 16 November 2001. Retrieved 20 April 2006.
Previously released as an MIT "Technical Memo" in April 1977, and published in Martin Gardner's Scientific American Mathematical recreations column
 Wayner, Peter (24 December 1997). "British Document Outlines Early Encryption Discovery". The New York Times. Retrieved 26 March 2015.
 Cocks, Clifford (20 November 1973). "A Note on 'Non-Secret Encryption'" (PDF). CESG Research Report.
 Singh, Simon (1999). The Code Book. Doubleday. pp. 279–292.
 Shannon, Claude; Weaver, Warren (1963). The Mathematical Theory of Communication. University of Illinois Press. ISBN 978-0-252-72548-7.
 "An Example of a Man-in-the-middle Attack Against Server Authenticated SSL-sessions" (PDF).
 Junod, Pascal (2001). On the Complexity of Matsui's Attack (PDF). Selected Areas in Cryptography. Lecture Notes in Computer Science. 2259. pp. 199–211. doi:10.1007/3-540-45537-X_16. ISBN 978-3-540-43066-7.
 Song, Dawn; Wagner, David A.; Tian, Xuqing (2001). "Timing Analysis of Keystrokes and Timing Attacks on SSH" (PDF). Tenth USENIX Security Symposium.
 Brands, S. (1994). "Untraceable Off-line Cash in Wallet with Observers". Untraceable Off-line Cash in Wallets with Observers. Advances in Cryptology—Proceedings of CRYPTO. Lecture Notes in Computer Science. 773. pp. 302–318. doi:10.1007/3-540-48329-2_26. ISBN 978-3-540-57766-9. Archived from the original on 26 July 2011.
 Babai, László (1985). "Trading group theory for randomness". Proceedings of the seventeenth annual ACM symposium on Theory of computing - STOC '85. Proceedings of the Seventeenth Annual Symposium on the Theory of Computing. Stoc '85. pp. 421–429. CiteSeerX 10.1.1.130.3397. doi:10.1145/22145.22192. ISBN 978-0-89791-151-1. S2CID 17981195.
 Goldwasser, S.; Micali, S.; Rackoff, C. (1989). "The Knowledge Complexity of Interactive Proof Systems". SIAM Journal on Computing. 18 (1): 186–208. CiteSeerX 10.1.1.397.4002. doi:10.1137/0218012.
 Blakley, G. (June 1979). "Safeguarding cryptographic keys". Proceedings of AFIPS 1979. 48: 313–317.
 Shamir, A. (1979). "How to share a secret". Communications of the ACM. 22 (11): 612–613. doi:10.1145/359168.359176. S2CID 16321225.
 "6.5.1 What Are the Cryptographic Policies of Some Countries?". RSA Laboratories. Retrieved 26 March 2015.
 Rosenoer, Jonathan (1995). "Cryptography & Speech". CyberLaw. Missing or empty |url= (help)
"Archived copy". Archived from the original on 1 December 2005. Retrieved 23 June 2006.
 "Case Closed on Zimmermann PGP Investigation". IEEE Computer Society's Technical Committee on Security and Privacy. 14 February 1996. Retrieved 26 March 2015.
 Levy, Steven (2001). Crypto: How the Code Rebels Beat the Government—Saving Privacy in the Digital Age. Penguin Books. p. 56. ISBN 978-0-14-024432-8. OCLC 244148644.
 "Bernstein v USDOJ". Electronic Privacy Information Center. United States Court of Appeals for the Ninth Circuit. 6 May 1999. Retrieved 26 March 2015.
 "Dual-use List – Category 5 – Part 2 – "Information Security"" (PDF). Wassenaar Arrangement. Retrieved 26 March 2015.
 ".4 United States Cryptography Export/Import Laws". RSA Laboratories. Retrieved 26 March 2015.
 Schneier, Bruce (15 June 2000). "The Data Encryption Standard (DES)". Crypto-Gram. Retrieved 26 March 2015.
 Coppersmith, D. (May 1994). "The Data Encryption Standard (DES) and its strength against attacks" (PDF). IBM Journal of Research and Development. 38 (3): 243–250. doi:10.1147/rd.383.0243. Retrieved 26 March 2015.
 Biham, E.; Shamir, A. (1991). "Differential cryptanalysis of DES-like cryptosystems". Journal of Cryptology. 4 (1): 3–72. doi:10.1007/bf00630563. S2CID 206783462.
 "The Digital Millennium Copyright Act of 1998" (PDF). United States Copyright Office. Retrieved 26 March 2015.
 Ferguson, Niels (15 August 2001). "Censorship in action: why I don't publish my HDCP results". Missing or empty |url= (help)
"Archived copy". Archived from the original on 1 December 2001. Retrieved 16 February 2009.
 Schneier, Bruce (6 August 2001). "Arrest of Computer Researcher Is Arrest of First Amendment Rights". InternetWeek. Retrieved 7 March 2017.
 Williams, Christopher (11 August 2009). "Two convicted for refusal to decrypt data". The Register. Retrieved 26 March 2015.
 Williams, Christopher (24 November 2009). "UK jails schizophrenic for refusal to decrypt files". The Register. Retrieved 26 March 2015.
 Ingold, John (4 January 2012). "Password case reframes Fifth Amendment rights in context of digital world". The Denver Post. Retrieved 26 March 2015.
 Leyden, John (13 July 2011). "US court test for rights not to hand over crypto keys". The Register. Retrieved 26 March 2015.
 "Order Granting Application under the All Writs Act Requiring Defendant Fricosu to Assist in the Execution of Previously Issued Search Warrants" (PDF). United States District Court for the District of Colorado. Retrieved 26 March 2015.
Further reading
Further information: Books on cryptography
Becket, B (1988). Introduction to Cryptology. Blackwell Scientific Publications. ISBN 978-0-632-01836-9. OCLC 16832704. Excellent coverage of many classical ciphers and cryptography concepts and of the "modern" DES and RSA systems.
Cryptography and Mathematics by Bernhard Esslinger, 200 pages, part of the free open-source package CrypTool, PDF download at the Wayback Machine (archived 22 July 2011). CrypTool is the most widespread e-learning program about cryptography and cryptanalysis, open source.
In Code: A Mathematical Journey by Sarah Flannery (with David Flannery). Popular account of Sarah's award-winning project on public-key cryptography, co-written with her father.
James Gannon, Stealing Secrets, Telling Lies: How Spies and Codebreakers Helped Shape the Twentieth Century, Washington, D.C., Brassey's, 2001, ISBN 1-57488-367-4.
Oded Goldreich, Foundations of Cryptography, in two volumes, Cambridge University Press, 2001 and 2004.
Introduction to Modern Cryptography by Jonathan Katz and Yehuda Lindell.
Alvin's Secret Code by Clifford B. Hicks (children's novel that introduces some basic cryptography and cryptanalysis).
Ibrahim A. Al-Kadi, "The Origins of Cryptology: the Arab Contributions," Cryptologia, vol. 16, no. 2 (April 1992), pp. 97–126.
Christof Paar, Jan Pelzl, Understanding Cryptography, A Textbook for Students and Practitioners. Springer, 2009. (Slides, online cryptography lectures and other information are available on the companion web site.) Very accessible introduction to practical cryptography for non-mathematicians.
Introduction to Modern Cryptography by Phillip Rogaway and Mihir Bellare, a mathematical introduction to theoretical cryptography including reduction-based security proofs. PDF download.
Johann-Christoph Woltag, 'Coded Communications (Encryption)' in Rüdiger Wolfrum (ed) Max Planck Encyclopedia of Public International Law (Oxford University Press 2009).
"Max Planck Encyclopedia of Public International Law"., giving an overview of international law issues regarding cryptography.
Jonathan Arbib & John Dwyer, Discrete Mathematics for Cryptography, 1st Edition ISBN 978-1-907934-01-8.
Stallings, William (March 2013). Cryptography and Network Security: Principles and Practice (6th ed.). Prentice Hall. ISBN 978-0-13-335469-0.
External links
	Wikiquote has quotations related to: Cryptography
	Wikibooks has more on the topic of: Cryptography
	At Wikiversity, you can learn more and teach others about Cryptography at the Department of Cryptography
	Wikisource has the text of the 1911 Encyclopædia Britannica article Cryptography.
Library resources about
Cryptography
Online books
Resources in your library
Resources in other libraries
 The dictionary definition of cryptography at Wiktionary
 Media related to Cryptography at Wikimedia Commons
Cryptography on In Our Time at the BBC
Crypto Glossary and Dictionary of Technical Cryptography
NSA's CryptoKids.
Overview and Applications of Cryptology by the CrypTool Team; PDF; 3.8 MB. July 2008
A Course in Cryptography by Raphael Pass & Abhi Shelat – offered at Cornell in the form of lecture notes.
For more on the use of cryptographic elements in fiction, see: Dooley, John F., William and Marilyn Ingersoll Professor of Computer Science, Knox College (23 August 2012). "Cryptology in Fiction".
The George Fabyan Collection at the Library of Congress has early editions of works of seventeenth-century English literature, publications relating to cryptography.
vte
Cryptography
vte
Espionage
vte
Hidden messages
vte
Intelligence management
Authority control Edit this at Wikidata	
BNE: XX4659806NARA: 10644644
Categories: CryptographyBanking technologyFormal sciencesApplied mathematics
Navigation menu
Not logged inTalkContributionsCreate accountLog in
ArticleTalk
ReadEditView historySearch
Search Wikipedia
Main page
Contents
Current events
Random article
About Wikipedia
Contact us
Donate
Contribute
Help
Learn to edit
Community portal
Recent changes
Upload file
Tools
What links here
Related changes
Special pages
Permanent link
Page information
Cite this page
Wikidata item
Print/export
Download as PDF
Printable version
In other projects
Wikimedia Commons
Wikibooks
Wikiquote
Wikiversity

Languages
العربية
Azərbaycanca
فارسی
Հայերեն
עברית
ქართული
Қазақша
کوردی
中文
82 more
Edit links
This page was last edited on 23 October 2020, at 19:28 (UTC).
Text is available under the Creative Commons Attribution-ShareAlike License; additional terms may apply. By using this site, you agree to the Terms of Use and Privacy Policy. Wikipedia® is a registered trademark of the Wikimedia Foundation, Inc., a non-profit organization.
