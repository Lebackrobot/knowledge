# 🧩 Unit Tests

## Conceito

Consiste em testar a menor parte testável (funções e métodos) de um software.

<img title="" src="file:///C:/Users/Pedro_Santos2/Downloads/unit-tests.jpg" alt="" width="621" data-align="center">



*"Testes unitários, assim como qualquer teste automatizados não servem principalmente para verificar se uma função específica está funcionando, mas sim para garantir que aplicação continue funcionando após alguma alteração em sua base de código."*



---

### Tipos de testes

- Testes unitários

- Testes de integração

- Testes de E2E

---

## Design Patterns

No curso conheci dois Patterns, mas não entendo completamente diferença



-  Given, When, Then

- Triple A (Arrange, Act , Assert)



---

## Aproachs

Existem escolas de pensamento que diferem em suas abordagens de desenvolvimento de testes.



- [x] TDD

- [ ] BD

---

## 🏷️ Markers

São labels que podem ser inseridas nos testes unitários. 



```python
import pytest

@pytest.mark.webtest
def test_send_http_request():
    assert True
```



Para evitar `warnings` sobre os markers não registrados, podemos registrar markers personalizados em um arquivo `pytest.ini`.



```
[pytest]

markers =
    webtest: Mark test with HTTP requests.
```



---

## Cobertura de Testes (pytest-cov)

### Instalação:

É necessário instalar o plugin de cobertura pytest coverage

```bash
pip install pytest-cov
```



### Medindo a cobertura de testes

Para medir a cobertura de testes, basta executar um comando passando o diretório que tenha os módulos que você deseja testar.



```bash
# Cobertura de testes do diretório src
pytest --cov='src'


# Cobertura de testes do diretório src
pytest --cov='src' --cov-report term-missing
```


