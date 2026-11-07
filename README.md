
import random

print("🤖 Welcome to My AI!")
print("Type 'bye' to exit.")

responses = {
    "hello": ["Hello! How are you?", "Hey there!", "Hi! What's up?"],
    "how are you": ["I'm doing great!", "I'm ready to help!"],
    "who are you": ["I'm your personal AI assistant!"],
    "bye": ["Goodbye! See you later!"]
}

while True:
    user = input("You: ").lower()

    if user == "bye":
        print("AI: Goodbye!")
        break

    answer = None

    for keyword in responses:
        if keyword in user:
            answer = random.choice(responses[keyword])
            break

    if answer:
        print("AI:", answer)
    else:
        print("AI: Interesting! Tell me more.")
