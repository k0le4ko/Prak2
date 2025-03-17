# Проєкт на Python
| def process_text(text):
    # Розділення тексту на слова
    words = text.split()
    
    # Знаходимо слова з парними номерами, які містять непарну кількість літер
    even_position_odd_length_words = [
        words[i] for i in range(1, len(words), 2) if len(words[i]) % 2 != 0
    ]
    
    print("")
    # Вивід слів з парними номерами, які мають непарну кількість літер
    print("Слова з парними номерами та непарною кількістю літер:")
    for word in even_position_odd_length_words:
        print(word)
    
    # Видаляємо наступні входження першої літери в кожному слові
    modified_words = [remove_next_occurrences_of_first_letter(word) for word in words]
    
    # Вивід модифікованого тексту
    print("\nТекст з видаленими наступними входженнями першої літери у кожному слові:")
    print(" ".join(modified_words))


def remove_next_occurrences_of_first_letter(word):
    # Видаляємо всі наступні входження першої літери в слові
    if len(word) < 2:
        return word
    first_char = word[0]
    result = first_char + "".join([char for char in word[1:] if char != first_char])
    return result

# Ввід довільного тексту для перевірки програми
text = input("Введіть текст для перевірки:")
process_text(text) | 
| --- |

**Блок-схема алгоритму роботи програми**
