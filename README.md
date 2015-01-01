papers
======

A git-annex repository of academic papers. Mostly machine learning related.

Using
-----

First install `git` and `git-annex`. Then:

```sh
git clone git://github.com/rejuvyesh/papers
git-annex init local
git-annex get .
```

If you want just some particular paper:

```
git-annex get deep-learning/2011-deep-sparse-rectifier-neural-networks.pdf
```

Please open an issue if you cannot download any paper so that I can mirror them.

How I created this?
-------------------

```sh
cd papers
git init
git remote add origin git@github.com/rejuvyesh/papers
git-annex init laptop
git-annex addurl --file deep-learning/1997-bain-on-neural-networks.pdf http://deeplearning.cs.cmu.edu/pdfs/Bain.On.Neural.Networks.pdf
git-annex add .
git commit -m "papers"
git config remote.origin.annex-ignore true  # Because GitHub doesn't store annexed content. 
git push origin master git-annex
```
