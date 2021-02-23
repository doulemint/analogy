# 函数数据分析
## hico_api.py
 - **get_vocab_visualphrases** : 添加所有单词到Vocabulary类 (['person', predicate, objname], 'noun-verb-noun')
 - **_build_db(annotations)** : 
  - **_init_coco**
    - self.classes: 添加所有coco数据中的名词词汇， e.i. ('background', 'noun')
    - json_category_id_to_contiguous_id
  - **_add_relationships**
    - all_relationships: [im_id, sub_id, obj_id, rel_cat] sub_id和obj_id: 是subject和object在im_id这个字典item里面的index
    - **def multilabel_transform()**: 
    - **def build_label()**: 
  
 - **get_training_candidates**: 
 - **get_idx_between_vocab**
