T = TypeVar('T', bound='PrefixEnum')

def PrefixEnum(prefix: str, /) -> Type[enum.StrEnum]:
    class PrefixEnum(enum.StrEnum):
        def __new__(cls: Type[T], value: str) -> T:
            value = f"{prefix}_{value}"
            obj = str.__new__(cls, value)
            obj._value_ = value
            return obj
