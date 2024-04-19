```shell
# Instalar python a partir da Windows App Store
pip install --user pipx
python -m pipx install poetry
# Liberar criação de arquivos com path longo para evitar erros de instalação nos módulos do poetry
# https://stackoverflow.com/questions/72352528/how-to-fix-winerror-206-the-filename-or-extension-is-too-long-error?noredirect=1
poetry add "<module>"

poetry run ipython kernel install --user --name=<KERNEL_NAME>
poetry run jupyter notebook
```