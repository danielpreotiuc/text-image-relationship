# Text-Image Relationship in Tweets

An annotated Twitter data setof image tweets annotated with four classes which express whether the text or the image provides additional information to the other modality.

## Paper: https://www.aclweb.org/anthology/P19-1272.pdf

## Presentation: https://www.aclweb.org/anthology/attachments/P19-1272.Presentation.pdf

## Data

The data set file (textimage.csv) contains tweet_ids, annotated labels and identifies the data splits used in the original paper.

For accessing the full data set, including the raw tweet text and images, please contact the authors: Alakananda (v.alakananda@gmail.com) and Daniel (danielpr@gmail.com)

## Task description:

We define the types of semantic relationships that can exist between the content of the text and the image by splitting them into two tasks. Combining the labels of the two binary tasks described below gives rise to four types of text-image relationships (identified in the file by the non-zero value in the following columns: "image_adds_text_repr","image_adds_text_notrepr","image_notadds_text_repr","image_notadds_text_notrepr").

The first task (column "text_is_represented") is centered on the role of the text to the tweet’s semantics and focuses on identifying if there is semantic overlap between the context of the text and the image. This task is the defined using the following guidelines:
1. Some or all of the content words in the text are represented in the image ("text_is_represented" value of 1)
2. None of the content words in the text are represented in the image ("text_is_represented" value of 0):
- None of the content words are represented in the image, or
- The text is only a comment about the content of the image, or
- The text expresses a feeling or emotion about the content of the image, or
- The text only makes a reference to something shown in the image, or
- The text is unrelated to the image

The second task – referred to as the image task (column "image_adds") – focuses on the role of the image to the semantics of the tweet and aims to identify if the image’s content contributes with additional information to the meaning of the tweet beyond the text, as judged by an independent third party. This task is defined and annotated using the following guidelines:
1. Image has additional content that represents the meaning of the text and the image ("image_adds" value of 1):
- Image contains other text that adds additional meaning to the text, or
- Image depicts something that adds information to the text or
- Image contains other entities that are referenced by the text.
2. Image does not add additional content that represents the meaning of text+image ("image_adds" value of 0)

More information and examples are depicted in the paper: https://www.aclweb.org/anthology/P19-1272.pdf


Citation:

```
@inproceedings{vempala-preotiuc-pietro-2019-categorizing,
    title = "Categorizing and Inferring the Relationship between the Text and Image of {T}witter Posts",
    author = "Vempala, Alakananda  and
      Preo{\c{t}}iuc-Pietro, Daniel",
    booktitle = "Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics",
    month = jul,
    year = "2019",
    address = "Florence, Italy",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/P19-1272",
    doi = "10.18653/v1/P19-1272",
    pages = "2830--2840",
    abstract = "Text in social media posts is frequently accompanied by images in order to provide content, supply context, or to express feelings. This paper studies how the meaning of the entire tweet is composed through the relationship between its textual content and its image. We build and release a data set of image tweets annotated with four classes which express whether the text or the image provides additional information to the other modality. We show that by combining the text and image information, we can build a machine learning approach that accurately distinguishes between the relationship types. Further, we derive insights into how these relationships are materialized through text and image content analysis and how they are impacted by user demographic traits. These methods can be used in several downstream applications including pre-training image tagging models, collecting distantly supervised data for image captioning, and can be directly used in end-user applications to optimize screen estate.",
}
```
