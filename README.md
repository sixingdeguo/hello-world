@unique
class ChatRole(str, Enum):
    SYSTEM = "SYSTEM"
    HUMAN = "HUMAN"
    AI = "AI"
    EXTRA = "EXTRA"
