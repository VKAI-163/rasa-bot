## Installed python dependencies

```
pip3 install rasa_core
pip3 install rasa_nlu
pip3 install spacy
pip3 install sklearn_crfsuite
```
To Install Models:
```
python3 -m spacy download en_core_web_md
python3 -m spacy link en_core_web_md en
```

For "ValueError: unknown locale: UTF-8"
```
export LC_ALL=en_US.UTF-8
```