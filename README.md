# Projeto Bandcamp e Generic View
> Essa API é como uma cópia da base do site BandCamp, com criação de usuários, criação de álbuns, músicas, entre outros.

## Rotas da API

| Rotas | Verbo HTTP | Objetivo|
| ------- |:-----------:|--------:|
|/api/users/ | POST | Criação de usuário
|/api/users/login/ | POST | Autenticação do usuário
|/api/users/user_id/ | GET | Busca de usuário por id
|/api/users/user_id/ | PATCH | Atualizar usuário
|/api/users/user_id/ | DELETE | Deleção de usuário
|/api/albums/ | POST | Criação de álbum
|/api/albums/ | GET | Listagem de álbuns
|/api/albums/album_id/songs/ | GET | Busca de sons de um álbum por id
|/api/movies/album_id/songs/ | POST | Criação de música

## Instalação dos pacotes de teste

- Verifique se os pacotes `pytest` e/ou `pytest-testdox` estão instalados globalmente em seu sistema:
```shell
pip list
```
- Caso seja listado o `pytest` e/ou `pytest-testdox` e/ou `pytest-django` em seu ambiente global, utilize os seguintes comando para desinstalá-los globalmente:
```shell
pip uninstall pytest
```

```shell
pip uninstall pytest-testdox
```

```shell
pip uninstall pytest-django
```

A partir disso, prossiga com os passos:

1. Crie seu ambiente virtual:
```bash
python -m venv venv
```

2. Ative seu venv:
```bash
# Linux:
source venv/bin/activate

# Windows (Powershell):
.\venv\Scripts\activate

# Windows (Git Bash):
source venv/Scripts/activate
```

3. Instale o pacote `pytest-testdox`:
```shell
pip install pytest-testdox pytest-django
```


4. Agora é só rodar os testes no diretório principal do projeto:
```shell
pytest --testdox -vvs
```

5. Caso queira um log mais resumido, basta executar com os testes sem as flags **verbose**:
```shell
pytest --testdox
```

## Rodando os testes por partes

Caso você tenha interesse em rodar apenas um diretório de testes específico, pode utilizar o comando:

- Rodando testes de users:
```python
pytest --testdox -vvs tests/users/
```

- Rodando testes de albums:
```python
pytest --testdox -vvs tests/albums/
```

- Rodando testes de songs:
```python
pytest --testdox -vvs tests/songs/
```