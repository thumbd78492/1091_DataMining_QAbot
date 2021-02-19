# 1091_DataMining_QAbot

##BOT_build_data.ipynb
Doing data preprocessing
把維基的資料和PTT八卦版的新聞做切字、詞性分析
製作成以下四種檔案：

**IDTitle_content_string.txt**
格式：ID:TITLE WORD1 WORD2 WORD3 ...
以行為單位
**new_PTT_IDTitle_content_string.txt**
格式：ID:TITLE WORD1 WORD2 WORD3 ...
以行為單位
之後將這兩者merge起來。

**word_entropy_table.pickle**
一個詞對應到entropy的dictionary
如：
entropyDict['一個'] : 1.3884529392843121
entropyDict['劉備'] : 10.011451220629336

**word_ID_table.pickle**
一個詞對應到出現的文章ID List的dictionary
如：
word_ID_table['華視新聞'] = ['1588950762', '1589003461', '1589091111', ...]


##BOT_scoring_withPTT.ipynb
Doing the Q&A
使用前處理後的資料來做問答。
