---
layout: post
title:  Cascading getattr
categories: [Python,Esoteric,Snippet]
excerpt: This is just a snippet I made while messing around with getattr(). Valid python, all for fun.
---

## Hello World
```python
getattr(
    getattr(
        getattr(
            getattr(
                getattr(
                    getattr(
                        getattr(
                            getattr(
                                getattr(
                                    getattr(
                                        getattr(
                                            getattr(
                                                getattr(
                                                    getattr(
                                                        getattr(
                                                            getattr(
                                                                getattr(
                                                                    getattr(
                                                                        getattr(
                                                                            getattr(
                                                                                getattr(
                                                                                    getattr(
                                                                                        getattr(
                                                                                            getattr(
                                                                                                getattr,
                                                                                                '__call__'),
                                                                                            '__call__'),
                                                                                        '__call__'),
                                                                                    '__call__'),
                                                                                '__call__'),
                                                                            '__call__'),
                                                                        '__call__'),
                                                                    '__call__'),
                                                                '__call__'),
                                                            '__call__'),
                                                        '__call__'),
                                                    '__call__'),
                                                '__call__'),
                                            '__call__'),
                                        '__call__'),
                                    '__call__'),
                                '__call__'),
                            '__call__'),
                        '__call__'),
                    '__call__'),
                '__call__'),
            '__call__'),
        '__call__'),
    '__call__'
)(print, '__call__')('hello world')
```
