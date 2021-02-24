# 函数数据分析
## hico_api.py
 - **get_vocab_visualphrases** : 添加所有单词到Vocabulary类 (['person', predicate, objname], 'noun-verb-noun')
 - **_build_db(annotations)** :  实际上一张图中每一个物体会有至少4个的box框圈出来。然后 将4x4相互关联_add_relationships
  - **_add_objects** ：这个函数主要是将annotations里面所有的box,object名字存入db数据库。但是此时只有名词，只完成了detection
  - **_init_coco**
    - self.classes: 添加所有coco数据中的名词词汇， e.i. ('background', 'noun')
    - json_category_id_to_contiguous_id
  - **_add_relationships**
    - all_relationships: [im_id, sub_id, obj_id, rel_cat] sub_id和obj_id: 是subject和object在im_id这个字典item里面的index
     - labels: 为subject所发生的动作的one hot encoding
    - **def multilabel_transform()**: 
    - **def build_label()**: 
 - **populate_candidates**: 为false candidates之间建立关系
 - **label_candidates** : 添加了一些false的candidates
 - **get_training_candidates**: 
 - **get_idx_between_vocab**
## dataset.py
 - **get_scores**: db[im_id]['obj_scores']
 - **get_labels_predicates**: db[im_id]['labels_r']
 - **filter_pairs_neg**: db[im_id]['labels_r'][idx,0]==1 为negative
 - **filter_pairs_pos**: np.where(np.any(db[im_id]['labels_r'][:,1:], axis=1))[0]
