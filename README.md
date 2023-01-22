#import nltk
from nltk.chat.util import Chat, reflections
pairs = [
    [
        r"mi nombre es (.*)",
        ["Hola , ¿cómo estás hoy?"]
    ],
    [
        r"hola|holi|hey",
        ["Hola", "Hola, ¿cómo estás?"]
    ],
    [
        r"¿cómo te llamas?",
        ["Mi nombre es Yuuki, ¿cómo puedo ayudarte?"]
    ],
    [
        r"cómo estas?",
        ["Estoy bien, ¿y tú?"]
    ],
    [
        r"lo siento (.*)",
        ["No hay problema","No te preocupes, no pasa nada"]
    ],
    [
        r"estoy bien",
        ["Me alegra escuchar eso, ¿cómo puedo ayudarte?"]
    ],

    [
        r"adios",
        ["Adiós, cuídate. Fue agradable hablar contigo :) "]
    ],
]
chatbot = Chat(pairs, reflections)
chatbot.converse()
