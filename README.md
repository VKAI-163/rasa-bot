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

Lets run to train our NLU model
```
python -m rasa_nlu.train -c nlu_model_config.json --fixed_model_name current

```
To train the dialogue model, run:
```
python3 -m rasa_core.train -s data/stories.md -d domain.yml -o models/dialogue --epochs 300
```

Here we’ll just talk to the bot on the command line:
```
python3 -m rasa_core.run -d models/dialogue -u models/nlu/default/current
```

Reference:
https://core.rasa.com/tutorial_basics.html#tutorial-basics