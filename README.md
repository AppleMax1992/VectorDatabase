# VectorDatabase
1. 运行环境python3.7.9 nootbook pip install weaviate-client markdown bs4
2. 两个md file在dataset中作为输入数据, 运行weaviate.ipynb即可
3. 从md file转html, 从html中parse h1 tag中的内容作为title, 第二行中p tag中的内容作为author, 其中内容通过正则去掉特殊字符. 其余的所有字段通过bs4抽取文字内容.
4. 所有文件抽取title, author, content内容之后转化为dataframe作为输入.
5. bert-base-uncased 能处理的字段只有512, 因此选sentence-transformers/facebook-dpr-question_encoder-single-nq-base作为encoder
