# aiodine

aiodine provides async-capable [dependency injection][di] in the style of [Pytest fixtures](https://docs.pytest.org/en/latest/fixture.html) for Python 3.6+.

## Installation

```
pip install aiodine
```

## Usage

aiodine revolves around two concepts: **providers** and **consumers**.

**Providers** make a _resource_ available to consumers within a certain _scope_.

Here's a "hello world" provider:

```python
import aiodine

@aiodine.provider
def hello():
    return "Hello, aiodine!"
```

Once a provider has been declared, it can be used by **consumers**. All a consumer has to do is declare the provider as one of its parameters, and aiodine will inject it at runtime.

Here's an example consumer:

```python
@aiodine.consumer
def show_friendly_message(hello):
    print(hello)

show_friendly_message()  # "Hello, aiodine!"
```

More usage tips to come.

## FAQ

### Why "aiodine"?

aiodine contains _aio_ as in _asyncio_, and _di_ as in [Dependency Injection][di] The last two letters are only there to make this library's name pronounce like _iodine_, the chemical element.

[di]: https://en.wikipedia.org/wiki/Dependency_injection
