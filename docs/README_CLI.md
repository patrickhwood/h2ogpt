### CLI chat

The CLI can be used instead of gradio by running for some base model, e.g.:
```bash
python generate.py --base_model=gptj --cli=True --answer_with_sources=False
```
and for LangChain run:
```bash
python src/make_db.py --user_path=user_path --collection_name=UserData
python generate.py --base_model=gptj --cli=True --langchain_mode=UserData --answer_with_sources=False
```
with documents in `user_path` folder, or directly run:
```bash
python generate.py --base_model=gptj --cli=True --langchain_mode=UserData --user_path=user_path --answer_with_sources=False
```
which will build the database first time.  One can also use any other models, like:
```bash
python generate.py --base_model=h2oai/h2ogpt-oig-oasst1-512-6_9b --cli=True --langchain_mode=UserData --user_path=user_path --answer_with_sources=False
```
or for LLaMa2:
```bash
python generate.py --base_model='llama' --prompt_type=llama2 --cli=True --langchain_mode=UserData --user_path=user_path --answer_with_sources=False
```

