from collections import defaultdict

def group_anagrams(words):
    anagrams = defaultdict(list)
    for word in words:
        anagrams[tuple(sorted(word))].append(word)
    return list(anagrams.values())

# Taking user input
words = input("Enter words separated by space: ").split()
print(group_anagrams(words))
