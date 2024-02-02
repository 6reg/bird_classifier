Install fastai and duckduckgo_search libraries...


```python
!pip install -Uqq fastai duckduckgo_search
```


```python
import duckduckgo_search
print(dir(duckduckgo_search))
```

    ['AsyncDDGS', 'DDGS', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__path__', '__spec__', '__version__', 'duckduckgo_search', 'duckduckgo_search_async', 'exceptions', 'logging', 'models', 'utils', 'version']



```python
!pip install fastbook
```

    Requirement already satisfied: fastbook in /opt/homebrew/lib/python3.11/site-packages (0.0.29)
    Requirement already satisfied: pip in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (23.2.1)
    Requirement already satisfied: packaging in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (23.1)
    Requirement already satisfied: fastai>=2.6 in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (2.7.14)
    Requirement already satisfied: graphviz in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (0.20.1)
    Requirement already satisfied: pandas in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (2.1.1)
    Requirement already satisfied: requests in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (2.31.0)
    Requirement already satisfied: transformers in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (4.33.3)
    Requirement already satisfied: datasets in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (2.16.1)
    Requirement already satisfied: ipywidgets<8 in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (7.8.1)
    Requirement already satisfied: sentencepiece in /opt/homebrew/lib/python3.11/site-packages (from fastbook) (0.1.99)
    Requirement already satisfied: fastdownload<2,>=0.0.5 in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (0.0.7)
    Requirement already satisfied: fastcore<1.6,>=1.5.29 in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (1.5.29)
    Requirement already satisfied: torchvision>=0.11 in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (0.17.0)
    Requirement already satisfied: matplotlib in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (3.7.1)
    Requirement already satisfied: pyyaml in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (6.0.1)
    Requirement already satisfied: fastprogress>=0.2.4 in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (1.0.3)
    Requirement already satisfied: pillow>=9.0.0 in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (9.5.0)
    Requirement already satisfied: scikit-learn in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (1.4.0)
    Requirement already satisfied: scipy in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (1.12.0)
    Requirement already satisfied: spacy<4 in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (3.7.2)
    Requirement already satisfied: torch<2.3,>=1.10 in /opt/homebrew/lib/python3.11/site-packages (from fastai>=2.6->fastbook) (2.2.0)
    Requirement already satisfied: comm>=0.1.3 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipywidgets<8->fastbook) (0.1.4)
    Requirement already satisfied: ipython-genutils~=0.2.0 in /opt/homebrew/lib/python3.11/site-packages (from ipywidgets<8->fastbook) (0.2.0)
    Requirement already satisfied: traitlets>=4.3.1 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipywidgets<8->fastbook) (5.11.2)
    Requirement already satisfied: widgetsnbextension~=3.6.6 in /opt/homebrew/lib/python3.11/site-packages (from ipywidgets<8->fastbook) (3.6.6)
    Requirement already satisfied: ipython>=4.0.0 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipywidgets<8->fastbook) (8.16.1)
    Requirement already satisfied: jupyterlab-widgets<3,>=1.0.0 in /opt/homebrew/lib/python3.11/site-packages (from ipywidgets<8->fastbook) (1.1.7)
    Requirement already satisfied: filelock in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (3.12.2)
    Requirement already satisfied: numpy>=1.17 in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (1.24.3)
    Requirement already satisfied: pyarrow>=8.0.0 in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (15.0.0)
    Requirement already satisfied: pyarrow-hotfix in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (0.6)
    Requirement already satisfied: dill<0.3.8,>=0.3.0 in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (0.3.7)
    Requirement already satisfied: tqdm>=4.62.1 in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (4.66.1)
    Requirement already satisfied: xxhash in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (3.4.1)
    Requirement already satisfied: multiprocess in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (0.70.15)
    Requirement already satisfied: fsspec[http]<=2023.10.0,>=2023.1.0 in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (2023.9.2)
    Requirement already satisfied: aiohttp in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (3.9.3)
    Requirement already satisfied: huggingface-hub>=0.19.4 in /opt/homebrew/lib/python3.11/site-packages (from datasets->fastbook) (0.20.3)
    Requirement already satisfied: charset-normalizer<4,>=2 in /opt/homebrew/lib/python3.11/site-packages (from requests->fastbook) (3.3.0)
    Requirement already satisfied: idna<4,>=2.5 in /opt/homebrew/lib/python3.11/site-packages (from requests->fastbook) (3.4)
    Requirement already satisfied: urllib3<3,>=1.21.1 in /opt/homebrew/lib/python3.11/site-packages (from requests->fastbook) (2.0.5)
    Requirement already satisfied: certifi>=2017.4.17 in /opt/homebrew/lib/python3.11/site-packages (from requests->fastbook) (2023.7.22)
    Requirement already satisfied: python-dateutil>=2.8.2 in /opt/homebrew/lib/python3.11/site-packages (from pandas->fastbook) (2.8.2)
    Requirement already satisfied: pytz>=2020.1 in /opt/homebrew/lib/python3.11/site-packages (from pandas->fastbook) (2023.3.post1)
    Requirement already satisfied: tzdata>=2022.1 in /opt/homebrew/lib/python3.11/site-packages (from pandas->fastbook) (2023.3)
    Requirement already satisfied: regex!=2019.12.17 in /opt/homebrew/lib/python3.11/site-packages (from transformers->fastbook) (2023.8.8)
    Requirement already satisfied: tokenizers!=0.11.3,<0.14,>=0.11.1 in /opt/homebrew/lib/python3.11/site-packages (from transformers->fastbook) (0.13.3)
    Requirement already satisfied: safetensors>=0.3.1 in /opt/homebrew/lib/python3.11/site-packages (from transformers->fastbook) (0.3.3)
    Requirement already satisfied: aiosignal>=1.1.2 in /opt/homebrew/lib/python3.11/site-packages (from aiohttp->datasets->fastbook) (1.3.1)
    Requirement already satisfied: attrs>=17.3.0 in /opt/homebrew/lib/python3.11/site-packages (from aiohttp->datasets->fastbook) (23.2.0)
    Requirement already satisfied: frozenlist>=1.1.1 in /opt/homebrew/lib/python3.11/site-packages (from aiohttp->datasets->fastbook) (1.4.1)
    Requirement already satisfied: multidict<7.0,>=4.5 in /opt/homebrew/lib/python3.11/site-packages (from aiohttp->datasets->fastbook) (6.0.4)
    Requirement already satisfied: yarl<2.0,>=1.0 in /opt/homebrew/lib/python3.11/site-packages (from aiohttp->datasets->fastbook) (1.9.4)
    Requirement already satisfied: typing-extensions>=3.7.4.3 in /opt/homebrew/lib/python3.11/site-packages (from huggingface-hub>=0.19.4->datasets->fastbook) (4.9.0)
    Requirement already satisfied: backcall in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (0.2.0)
    Requirement already satisfied: decorator in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (5.1.1)
    Requirement already satisfied: jedi>=0.16 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (0.19.1)
    Requirement already satisfied: matplotlib-inline in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (0.1.6)
    Requirement already satisfied: pickleshare in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (0.7.5)
    Requirement already satisfied: prompt-toolkit!=3.0.37,<3.1.0,>=3.0.30 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (3.0.39)
    Requirement already satisfied: pygments>=2.4.0 in /opt/homebrew/lib/python3.11/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (2.16.1)
    Requirement already satisfied: stack-data in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (0.6.3)
    Requirement already satisfied: pexpect>4.3 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (4.8.0)
    Requirement already satisfied: appnope in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipython>=4.0.0->ipywidgets<8->fastbook) (0.1.3)
    Requirement already satisfied: six>=1.5 in /opt/homebrew/lib/python3.11/site-packages (from python-dateutil>=2.8.2->pandas->fastbook) (1.16.0)
    Requirement already satisfied: spacy-legacy<3.1.0,>=3.0.11 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (3.0.12)
    Requirement already satisfied: spacy-loggers<2.0.0,>=1.0.0 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (1.0.5)
    Requirement already satisfied: murmurhash<1.1.0,>=0.28.0 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (1.0.10)
    Requirement already satisfied: cymem<2.1.0,>=2.0.2 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (2.0.8)
    Requirement already satisfied: preshed<3.1.0,>=3.0.2 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (3.0.9)
    Requirement already satisfied: thinc<8.3.0,>=8.1.8 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (8.2.2)
    Requirement already satisfied: wasabi<1.2.0,>=0.9.1 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (1.1.2)
    Requirement already satisfied: srsly<3.0.0,>=2.4.3 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (2.4.8)
    Requirement already satisfied: catalogue<2.1.0,>=2.0.6 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (2.0.10)
    Requirement already satisfied: weasel<0.4.0,>=0.1.0 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (0.3.4)
    Requirement already satisfied: typer<0.10.0,>=0.3.0 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (0.9.0)
    Requirement already satisfied: smart-open<7.0.0,>=5.2.1 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (6.4.0)
    Requirement already satisfied: pydantic!=1.8,!=1.8.1,<3.0.0,>=1.7.4 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (2.6.0)
    Requirement already satisfied: jinja2 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (3.1.2)
    Requirement already satisfied: setuptools in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (68.1.2)
    Requirement already satisfied: langcodes<4.0.0,>=3.2.0 in /opt/homebrew/lib/python3.11/site-packages (from spacy<4->fastai>=2.6->fastbook) (3.3.0)
    Requirement already satisfied: sympy in /opt/homebrew/lib/python3.11/site-packages (from torch<2.3,>=1.10->fastai>=2.6->fastbook) (1.12)
    Requirement already satisfied: networkx in /opt/homebrew/lib/python3.11/site-packages (from torch<2.3,>=1.10->fastai>=2.6->fastbook) (3.1)
    Requirement already satisfied: notebook>=4.4.1 in /opt/homebrew/lib/python3.11/site-packages (from widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (7.0.7)
    Requirement already satisfied: contourpy>=1.0.1 in /opt/homebrew/lib/python3.11/site-packages (from matplotlib->fastai>=2.6->fastbook) (1.0.7)
    Requirement already satisfied: cycler>=0.10 in /opt/homebrew/lib/python3.11/site-packages (from matplotlib->fastai>=2.6->fastbook) (0.11.0)
    Requirement already satisfied: fonttools>=4.22.0 in /opt/homebrew/lib/python3.11/site-packages (from matplotlib->fastai>=2.6->fastbook) (4.39.4)
    Requirement already satisfied: kiwisolver>=1.0.1 in /opt/homebrew/lib/python3.11/site-packages (from matplotlib->fastai>=2.6->fastbook) (1.4.4)
    Requirement already satisfied: pyparsing>=2.3.1 in /opt/homebrew/lib/python3.11/site-packages (from matplotlib->fastai>=2.6->fastbook) (3.0.9)
    Requirement already satisfied: joblib>=1.2.0 in /opt/homebrew/lib/python3.11/site-packages (from scikit-learn->fastai>=2.6->fastbook) (1.3.2)
    Requirement already satisfied: threadpoolctl>=2.0.0 in /opt/homebrew/lib/python3.11/site-packages (from scikit-learn->fastai>=2.6->fastbook) (3.2.0)
    Requirement already satisfied: parso<0.9.0,>=0.8.3 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from jedi>=0.16->ipython>=4.0.0->ipywidgets<8->fastbook) (0.8.3)
    Requirement already satisfied: jupyter-server<3,>=2.4.0 in /opt/homebrew/lib/python3.11/site-packages (from notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.12.5)
    Requirement already satisfied: jupyterlab-server<3,>=2.22.1 in /opt/homebrew/lib/python3.11/site-packages (from notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.25.2)
    Requirement already satisfied: jupyterlab<5,>=4.0.2 in /opt/homebrew/lib/python3.11/site-packages (from notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (4.0.12)
    Requirement already satisfied: notebook-shim<0.3,>=0.2 in /opt/homebrew/lib/python3.11/site-packages (from notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.2.3)
    Requirement already satisfied: tornado>=6.2.0 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (6.3.3)
    Requirement already satisfied: ptyprocess>=0.5 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from pexpect>4.3->ipython>=4.0.0->ipywidgets<8->fastbook) (0.7.0)
    Requirement already satisfied: wcwidth in /Users/gm/Library/Python/3.11/lib/python/site-packages (from prompt-toolkit!=3.0.37,<3.1.0,>=3.0.30->ipython>=4.0.0->ipywidgets<8->fastbook) (0.2.8)
    Requirement already satisfied: annotated-types>=0.4.0 in /opt/homebrew/lib/python3.11/site-packages (from pydantic!=1.8,!=1.8.1,<3.0.0,>=1.7.4->spacy<4->fastai>=2.6->fastbook) (0.6.0)
    Requirement already satisfied: pydantic-core==2.16.1 in /opt/homebrew/lib/python3.11/site-packages (from pydantic!=1.8,!=1.8.1,<3.0.0,>=1.7.4->spacy<4->fastai>=2.6->fastbook) (2.16.1)
    Requirement already satisfied: blis<0.8.0,>=0.7.8 in /opt/homebrew/lib/python3.11/site-packages (from thinc<8.3.0,>=8.1.8->spacy<4->fastai>=2.6->fastbook) (0.7.11)
    Requirement already satisfied: confection<1.0.0,>=0.0.1 in /opt/homebrew/lib/python3.11/site-packages (from thinc<8.3.0,>=8.1.8->spacy<4->fastai>=2.6->fastbook) (0.1.4)
    Requirement already satisfied: click<9.0.0,>=7.1.1 in /opt/homebrew/lib/python3.11/site-packages (from typer<0.10.0,>=0.3.0->spacy<4->fastai>=2.6->fastbook) (8.1.7)
    Requirement already satisfied: cloudpathlib<0.17.0,>=0.7.0 in /opt/homebrew/lib/python3.11/site-packages (from weasel<0.4.0,>=0.1.0->spacy<4->fastai>=2.6->fastbook) (0.16.0)
    Requirement already satisfied: MarkupSafe>=2.0 in /opt/homebrew/lib/python3.11/site-packages (from jinja2->spacy<4->fastai>=2.6->fastbook) (2.1.3)
    Requirement already satisfied: executing>=1.2.0 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from stack-data->ipython>=4.0.0->ipywidgets<8->fastbook) (2.0.0)
    Requirement already satisfied: asttokens>=2.1.0 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from stack-data->ipython>=4.0.0->ipywidgets<8->fastbook) (2.4.0)
    Requirement already satisfied: pure-eval in /Users/gm/Library/Python/3.11/lib/python/site-packages (from stack-data->ipython>=4.0.0->ipywidgets<8->fastbook) (0.2.2)
    Requirement already satisfied: mpmath>=0.19 in /opt/homebrew/lib/python3.11/site-packages (from sympy->torch<2.3,>=1.10->fastai>=2.6->fastbook) (1.3.0)
    Requirement already satisfied: anyio>=3.1.0 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (4.2.0)
    Requirement already satisfied: argon2-cffi in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (23.1.0)
    Requirement already satisfied: jupyter-client>=7.4.4 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (8.4.0)
    Requirement already satisfied: jupyter-core!=5.0.*,>=4.12 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (5.4.0)
    Requirement already satisfied: jupyter-events>=0.9.0 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.9.0)
    Requirement already satisfied: jupyter-server-terminals in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.5.2)
    Requirement already satisfied: nbconvert>=6.4.4 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (7.14.2)
    Requirement already satisfied: nbformat>=5.3.0 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (5.9.2)
    Requirement already satisfied: overrides in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (7.7.0)
    Requirement already satisfied: prometheus-client in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.19.0)
    Requirement already satisfied: pyzmq>=24 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (25.1.1)
    Requirement already satisfied: send2trash>=1.8.2 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.8.2)
    Requirement already satisfied: terminado>=0.8.3 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.18.0)
    Requirement already satisfied: websocket-client in /opt/homebrew/lib/python3.11/site-packages (from jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.7.0)
    Requirement already satisfied: async-lru>=1.0.0 in /opt/homebrew/lib/python3.11/site-packages (from jupyterlab<5,>=4.0.2->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.0.4)
    Requirement already satisfied: ipykernel in /Users/gm/Library/Python/3.11/lib/python/site-packages (from jupyterlab<5,>=4.0.2->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (6.25.2)
    Requirement already satisfied: jupyter-lsp>=2.0.0 in /opt/homebrew/lib/python3.11/site-packages (from jupyterlab<5,>=4.0.2->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.2.2)
    Requirement already satisfied: babel>=2.10 in /opt/homebrew/lib/python3.11/site-packages (from jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.14.0)
    Requirement already satisfied: json5>=0.9.0 in /opt/homebrew/lib/python3.11/site-packages (from jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.9.14)
    Requirement already satisfied: jsonschema>=4.18.0 in /opt/homebrew/lib/python3.11/site-packages (from jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (4.21.1)
    Requirement already satisfied: sniffio>=1.1 in /opt/homebrew/lib/python3.11/site-packages (from anyio>=3.1.0->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.3.0)
    Requirement already satisfied: jsonschema-specifications>=2023.03.6 in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2023.12.1)
    Requirement already satisfied: referencing>=0.28.4 in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.33.0)
    Requirement already satisfied: rpds-py>=0.7.1 in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.17.1)
    Requirement already satisfied: platformdirs>=2.5 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from jupyter-core!=5.0.*,>=4.12->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (3.11.0)
    Requirement already satisfied: python-json-logger>=2.0.4 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-events>=0.9.0->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.0.7)
    Requirement already satisfied: rfc3339-validator in /opt/homebrew/lib/python3.11/site-packages (from jupyter-events>=0.9.0->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.1.4)
    Requirement already satisfied: rfc3986-validator>=0.1.1 in /opt/homebrew/lib/python3.11/site-packages (from jupyter-events>=0.9.0->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.1.1)
    Requirement already satisfied: beautifulsoup4 in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (4.12.3)
    Requirement already satisfied: bleach!=5.0.0 in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (6.1.0)
    Requirement already satisfied: defusedxml in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.7.1)
    Requirement already satisfied: jupyterlab-pygments in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.3.0)
    Requirement already satisfied: mistune<4,>=2.0.3 in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (3.0.2)
    Requirement already satisfied: nbclient>=0.5.0 in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.9.0)
    Requirement already satisfied: pandocfilters>=1.4.1 in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.5.1)
    Requirement already satisfied: tinycss2 in /opt/homebrew/lib/python3.11/site-packages (from nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.2.1)
    Requirement already satisfied: fastjsonschema in /opt/homebrew/lib/python3.11/site-packages (from nbformat>=5.3.0->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.19.1)
    Requirement already satisfied: argon2-cffi-bindings in /opt/homebrew/lib/python3.11/site-packages (from argon2-cffi->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (21.2.0)
    Requirement already satisfied: debugpy>=1.6.5 in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipykernel->jupyterlab<5,>=4.0.2->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.8.0)
    Requirement already satisfied: nest-asyncio in /opt/homebrew/lib/python3.11/site-packages (from ipykernel->jupyterlab<5,>=4.0.2->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.6.0)
    Requirement already satisfied: psutil in /Users/gm/Library/Python/3.11/lib/python/site-packages (from ipykernel->jupyterlab<5,>=4.0.2->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (5.9.6)
    Requirement already satisfied: webencodings in /opt/homebrew/lib/python3.11/site-packages (from bleach!=5.0.0->nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (0.5.1)
    Requirement already satisfied: fqdn in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.5.1)
    Requirement already satisfied: isoduration in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (20.11.0)
    Requirement already satisfied: jsonpointer>1.13 in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.4)
    Requirement already satisfied: uri-template in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.3.0)
    Requirement already satisfied: webcolors>=1.11 in /opt/homebrew/lib/python3.11/site-packages (from jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.13)
    Requirement already satisfied: cffi>=1.0.1 in /opt/homebrew/lib/python3.11/site-packages (from argon2-cffi-bindings->argon2-cffi->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.16.0)
    Requirement already satisfied: soupsieve>1.2 in /opt/homebrew/lib/python3.11/site-packages (from beautifulsoup4->nbconvert>=6.4.4->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.5)
    Requirement already satisfied: pycparser in /opt/homebrew/lib/python3.11/site-packages (from cffi>=1.0.1->argon2-cffi-bindings->argon2-cffi->jupyter-server<3,>=2.4.0->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.21)
    Requirement already satisfied: arrow>=0.15.0 in /opt/homebrew/lib/python3.11/site-packages (from isoduration->jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (1.3.0)
    Requirement already satisfied: types-python-dateutil>=2.8.10 in /opt/homebrew/lib/python3.11/site-packages (from arrow>=0.15.0->isoduration->jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook>=4.4.1->widgetsnbextension~=3.6.6->ipywidgets<8->fastbook) (2.8.19.20240106)
    
    [1m[[0m[34;49mnotice[0m[1;39;49m][0m[39;49m A new release of pip is available: [0m[31;49m23.2.1[0m[39;49m -> [0m[32;49m23.3.2[0m
    [1m[[0m[34;49mnotice[0m[1;39;49m][0m[39;49m To update, run: [0m[32;49mpython3.11 -m pip install --upgrade pip[0m


Use fastbook for it's search_images_ddg method.
Define search_images which takes arbitrary query and returns list of urls.



```python
from fastbook import *

def search_images(term, max=30):
  print(f"Searching for '{term}'")
  return search_images_ddg(term, max_images=max)

urls = search_images_ddg('bird photos', max_images=1)
urls[0]
```




    'https://wallpapercave.com/wp/wp7039045.jpg'



Use 'download_url' function from 'fastdownload' module to save the image locally. Open and view it..


```python
from fastdownload import download_url
dest = 'bird.jpg'
download_url(urls[0], dest, show_progress=False)

from fastai.vision.all import *
im = Image.open(dest)
im.to_thumb(256,256)
```




    
![png](bird_classifier_files/bird_classifier_7_0.png)
    




```python
download_url(search_images_ddg('dog photos', max_images=1)[0], 'dog.jpg', show_progress=False)
Image.open('dog.jpg').to_thumb(256,256)
```




    
![png](bird_classifier_files/bird_classifier_8_0.png)
    




```python
# Define a tuple of search terms. These will be used to search for images
searches = 'dog', 'bird'
# Use Path function to define location
path = Path('bird_or_not')
# Give api extra time
from time import sleep
# Iterate over the searches tuple
for o in searches:
  # Create unique folder for each search term in the tuple
  dest = (path/o) # bird_or_not/{'dog', 'bird'}
  # Use mkdir to create the directory. exist_ok=True means it won't throw an error if the directory already exists. Parents=True means it will create the parent directory if it doesn't exist
  dest.mkdir(exist_ok=True, parents=True)

  download_images(dest, urls=search_images(f'{o} photo'))
  sleep(10)
  download_images(dest, urls=search_images(f'{o} sun photo'))
  sleep(10)
  download_images(dest, urls=search_images(f'{o} shade photo'))
  sleep(10)
  resize_images(path/o, max_size=400, dest=path/o)
```

    Searching for 'dog photo'
    Searching for 'dog sun photo'
    Searching for 'dog shade photo'
    Searching for 'bird photo'
    Searching for 'bird sun photo'
    Searching for 'bird shade photo'



```python
# Check data set for failed downloads
failed = verify_images(get_image_files(path))
failed.map(Path.unlink)
len(failed)
```




    6




```python
# Use `DataLoaders` to train the model. It's an object that contains
# a training set (images used to create model) and a validation set(
# images used to check accurcacy of model). The `DataBlock` function gives
# us this functionalitly.
dls = DataBlock(
  blocks=(ImageBlock, CategoryBlock), # inputs to model are images, outputs are categories
  get_items=get_image_files, # grab all images in the path
  splitter=RandomSplitter(valid_pct=0.2, seed=42), # split data into
  # training and validation sets randomly, using 20% for validation
  get_y=parent_label, # label is name of parent dir
  item_tfms=[Resize(192, method='squish')] # resize each
).dataloaders(path, bs=32) # bs==batch size

dls.show_batch(max_n=6)
```


    
![png](bird_classifier_files/bird_classifier_11_0.png)
    



```python
# train using computer vision model resnet18. Use fastai's fine_tune
# which auto sets best practices for fine tuning a pre trained model
# 'fine-tuning' means starting with a model soemone else trained with
# another dataset and adjusting the params so it works with your dataset

learn = vision_learner(dls, resnet18, metrics=error_rate)
learn.fine_tune(3)
```



<style>
    /* Turns off some styling */
    progress {
        /* gets rid of default border in Firefox and Opera. */
        border: none;
        /* Needs to be in here for Safari polyfill so background images work as expected. */
        background-size: auto;
    }
    progress:not([value]), progress:not([value])::-webkit-progress-bar {
        background: repeating-linear-gradient(45deg, #7e7e7e, #7e7e7e 10px, #5c5c5c 10px, #5c5c5c 20px);
    }
    .progress-bar-interrupted, .progress-bar-interrupted::-webkit-progress-bar {
        background: #F44336;
    }
</style>




<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>epoch</th>
      <th>train_loss</th>
      <th>valid_loss</th>
      <th>error_rate</th>
      <th>time</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>1.906563</td>
      <td>1.569970</td>
      <td>0.531915</td>
      <td>00:02</td>
    </tr>
  </tbody>
</table>




<style>
    /* Turns off some styling */
    progress {
        /* gets rid of default border in Firefox and Opera. */
        border: none;
        /* Needs to be in here for Safari polyfill so background images work as expected. */
        background-size: auto;
    }
    progress:not([value]), progress:not([value])::-webkit-progress-bar {
        background: repeating-linear-gradient(45deg, #7e7e7e, #7e7e7e 10px, #5c5c5c 10px, #5c5c5c 20px);
    }
    .progress-bar-interrupted, .progress-bar-interrupted::-webkit-progress-bar {
        background: #F44336;
    }
</style>




<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>epoch</th>
      <th>train_loss</th>
      <th>valid_loss</th>
      <th>error_rate</th>
      <th>time</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>1.195720</td>
      <td>2.022968</td>
      <td>0.606383</td>
      <td>00:03</td>
    </tr>
    <tr>
      <td>1</td>
      <td>1.110270</td>
      <td>2.487636</td>
      <td>0.638298</td>
      <td>00:02</td>
    </tr>
    <tr>
      <td>2</td>
      <td>1.021070</td>
      <td>2.499106</td>
      <td>0.648936</td>
      <td>00:02</td>
    </tr>
  </tbody>
</table>



```python

# Use the fine-tuned resnet18 to predict bird
is_bird,_,probs = learn.predict(PILImage.create('bird.jpg'))
# show 'bird.jpg'
print(f"This is a: {is_bird}.")
print(f"Probability it's a bird: {probs[0]:.4f}")
Image.open('bird.jpg').to_thumb(256,256)

```



<style>
    /* Turns off some styling */
    progress {
        /* gets rid of default border in Firefox and Opera. */
        border: none;
        /* Needs to be in here for Safari polyfill so background images work as expected. */
        background-size: auto;
    }
    progress:not([value]), progress:not([value])::-webkit-progress-bar {
        background: repeating-linear-gradient(45deg, #7e7e7e, #7e7e7e 10px, #5c5c5c 10px, #5c5c5c 20px);
    }
    .progress-bar-interrupted, .progress-bar-interrupted::-webkit-progress-bar {
        background: #F44336;
    }
</style>







    This is a: bird photos.
    Probability it's a bird: 0.3578





    
![png](bird_classifier_files/bird_classifier_13_3.png)
    




```python
!pwd
```

    /Users/gm/projects/ml/fastai

