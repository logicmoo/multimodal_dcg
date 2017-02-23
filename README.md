# multimodal_dcg
Reduce floundering of DCGs by constraining and narrowing search 

```prolog

 :- pack_install('https://github.com/TeamSPoon/pack_multimodal_dcg.git').

```


```prolog

:- use_module(library(multimodal_dcg)).


predicate_named(Pred) --> dcgAnd(theText(Text),dcgLenBetween(1,5)).

:- must(dcgAnd(dcgLenBetween(5,1),theText(_Text),[a,b,c],[])).
:- must(predicate_named(_P,[proper,-,named],[])).


```
