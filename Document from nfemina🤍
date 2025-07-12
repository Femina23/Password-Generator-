
import random
import string

def generate_password(length=12, use_digits=True, use_specials=True):
    letters = string.ascii_letters
    digits = string.digits if use_digits else ''
    specials = string.punctuation if use_specials else ''

    all_chars = letters + digits + specials

    if not all_chars:
        return "Error: No characters selected for password generation."

    # Ensure at least one character from each selected category
    password = []
    password.append(random.choice(letters))
    if use_digits:
        password.append(random.choice(digits))
    if use_specials:
        password.append(random.choice(specials))

    while len(password) < length:
        password.append(random.choice(all_chars))

    random.shuffle(password)
    return ''.join(password)

# Example usage
print("Generated Password:", generate_password(length=16))
