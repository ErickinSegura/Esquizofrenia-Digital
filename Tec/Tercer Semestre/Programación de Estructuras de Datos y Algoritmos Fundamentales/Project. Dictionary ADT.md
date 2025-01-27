---
Nombre: Erick Segura Sánchez.
Matrícula: A01613821.
---
links: [[Programación de Estructuras de Datos y Algoritmos Fundamentales]]
Date: Friday 01/December/2023

Escogí un DictionaryADT para poder implementar una forma fácil de desarrollar diccionarios de cualquier tipo, y que tengan funciones útiles para el usuario. Podría ser utilizado para realizar diccionarios de lenguas que no son registradas fácilmente.

Ventajas:
Mejora una estructura de datos ya existente con mejores funciones.
Es fácil de comprender.
No necesitas conocer sobre estructuras de datos para utilizarla.

Desventajas:
Su implementación en C++ utiliza el concepto LIFO.
No ordena las palabras alfabéticamente.

Código en python
```python
class WordDictionary:

    def __init__(self):

        self.dictionary = {}

  

    def addWord(self, word, definition):

        self.dictionary[word] = definition

  

    def removeWord(self, word):

        if word in self.dictionary:

            del self.dictionary[word]

  

    def printDictionary(self):

        for word, definition in self.dictionary.items():

            print(f"{word} : {definition}")

  

    def searchWord(self, word):

        if word in self.dictionary:

            print(f"{word} : {self.dictionary[word]}")

        else:

            print("Word not found")

  

    def searchDefinition(self, definition):

        for word, defn in self.dictionary.items():

            if defn == definition:

                print(f"{word} : {defn}")

  

    def searchWordStartsWith(self, prefix):

        for word, defn in self.dictionary.items():

            if word.startswith(prefix):

                print(f"{word} : {defn}")

  

    def searchWordEndsWith(self, suffix):

        for word, defn in self.dictionary.items():

            if word.endswith(suffix):

                print(f"{word} : {defn}")

  

    def searchWordContains(self, substring):

        for word, defn in self.dictionary.items():

            if substring in word:

                print(f"{word} : {defn}")

  

    def searchWordLength(self, length):

        for word, defn in self.dictionary.items():

            if len(word) == length:

                print(f"{word} : {defn}")

  

    def searchWordLengthRange(self, min_length, max_length):

        for word, defn in self.dictionary.items():

            if min_length <= len(word) <= max_length:

                print(f"{word} : {defn}")

  
  

if __name__ == "__main__":

    wordDictionary = WordDictionary()

    wordDictionary.addWord("hello", "a greeting")

    wordDictionary.addWord("world", "the earth")

    wordDictionary.addWord("goodbye", "a farewell")

    wordDictionary.addWord("goodnight", "a farewell said in the evening or before going to sleep")

    wordDictionary.addWord("goodmorning", "a greeting said in the morning")

    wordDictionary.addWord("goodafternoon", "a greeting said in the afternoon")

    wordDictionary.addWord("goodday", "a greeting said in the day")

    wordDictionary.addWord("goodnight", "a farewell said in the evening or before going to sleep")

  

    wordDictionary.printDictionary()

    print()

  

    wordDictionary.searchWord("hello")

    print()

  

    wordDictionary.searchDefinition("a farewell said in the evening or before going to sleep")

    print()

  

    wordDictionary.searchWordStartsWith("good")

    print()

  

    wordDictionary.searchWordEndsWith("day")

    print()

  

    wordDictionary.searchWordContains("morning")

    print()

  

    wordDictionary.searchWordLength(5)

    print()

  

    wordDictionary.searchWordLengthRange(5, 7)

    print()

  

    wordDictionary.removeWord("hello")

    wordDictionary.printDictionary()
```