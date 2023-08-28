# Graph_To_Adjacency
Graph-To-Adjacency (GTA) is a tool that helps you to edit and quickly translate from graph topologies to adjacency matrices and vice versa. The matrices are represented in the following plain text format:
```
0 0 1 0 0 1 0 0 0 0
0 0 1 1 1 1 0 1 1 0
1 1 0 1 1 1 1 0 0 0
0 1 1 0 1 1 0 0 1 1
0 1 1 1 0 1 1 1 0 0
1 1 1 1 1 0 0 0 0 1
0 0 1 0 1 0 0 0 0 0
0 1 0 0 1 0 0 0 0 0
0 1 0 1 0 0 0 0 0 0
0 0 0 1 0 1 0 0 0 0
```

## Python import/export
Here are explained some tips to bring matrices from your python code to this tool, edit them manually and bring them back to your program.
My recommendation for pasting a numpy array `A` as importable text is :
```python
print('\n'.join([' '.join(list(ai_.astype(int).astype(str))) for ai_ in list(A)]))
```


On the other hand, for importing from a text string `txt` to a numpy array `A`:
```python

txt = '''
0 0 1 0 0 1 0 0 0 0
0 0 1 1 1 1 0 1 1 0
1 1 0 1 1 1 1 0 0 0
0 1 1 0 1 1 0 0 1 1
0 1 1 1 0 1 1 1 0 0
1 1 1 1 1 0 0 0 0 1
0 0 1 0 1 0 0 0 0 0
0 1 0 0 1 0 0 0 0 0
0 1 0 1 0 0 0 0 0 0
0 0 0 1 0 1 0 0 0 0
'''
A = np.genfromtxt(txt.splitlines())
```
