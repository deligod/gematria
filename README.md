# gematria
gematria calculator
touch gematria_calculator.py
# Define the mappings
first_ordinal = {chr(i + 96): i for i in range(1, 27)}
second_ordinal = {chr(123 - i): i for i in range(1, 27)}
third_ordinal = {chr(i + 96): (i % 9 if i % 9 != 0 else 9) for i in range(1, 27)}
fourth_ordinal = {chr(123 - i): (i % 9 if i % 9 != 0 else 9) for i in range(1, 27)}

# Function to calculate gematria value
def gematria_calculator(word, mapping):
    return sum(mapping[char] for char in word.lower() if char in mapping)

# Example usage
if __name__ == "__main__":
    word = input("Enter a word: ")

    first_value = gematria_calculator(word, first_ordinal)
    second_value = gematria_calculator(word, second_ordinal)
    third_value = gematria_calculator(word, third_ordinal)
    fourth_value = gematria_calculator(word, fourth_ordinal)

    print(f"First Ordinal Value: {first_value}")
    print(f"Second Ordinal Value: {second_value}")
    print(f"Third Ordinal Value: {third_value}")
    print(f"Fourth Ordinal Value: {fourth_value}")
git add gematria_calculator.py
git commit -m "Add gematria calculator script"
git push origin main


