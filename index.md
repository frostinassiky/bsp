## Boundary-sensitive Pre-training for Temporal Localization in Videos （ICCV'2021）
You can use the [editor on GitHub](https://github.com/frostinassiky/bsp/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Overview

Many video analysis tasks require temporal localization for the detection of content changes. However, most existing models developed for these tasks are pre-trained on general video action classification tasks. This is due to large scale annotation of temporal boundaries in untrimmed videos being expensive. Therefore, no suitable datasets exist that enable pre-training in a manner sensitive to temporal boundaries. In this paper for the first time, we investigate model pre-training for temporal localization by introducing a novel boundary-sensitive pretext (BSP) task. Instead of relying on costly manual annotations of temporal boundaries, we propose to synthesize temporal boundaries in existing video action classification datasets. By defining different ways of synthesizing boundaries, BSP can then be simply conducted in a self-supervised manner via the classification of the boundary types. This enables the learning of video representations that are much more transferable to downstream temporal localization tasks. Extensive experiments show that the proposed BSP is superior and complementary to the existing action classification-based pre-training counterpart, and achieves new state-of-the-art performance on several temporal localization tasks.

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/frostinassiky/bsp/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

### Bibtex
```
@InProceedings{xu2020bsp,
author = {Mengmeng Xu, Juan-Manuel Perez-Rua, Victor Escorcia, Brais Martinez, Xiatian Zhu, Li Zhang, Bernard Ghanem, Tao Xiang},
title = {G-TAD: Sub-Graph Localization for Temporal Action Detection},
booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
month = {Oct},
year = {2021}
}
```

### Contact
mengmeng.xu[at]kaust.edu.sa
