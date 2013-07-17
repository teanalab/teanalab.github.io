## Как добавить пост

1.  Идем [сюда](http://prose.io/#CLLKazan/issst-site/tree/master/_posts) для создания русских постов,
[cюда](http://prose.io/#CLLKazan/issst-site/tree/master/_posts/en) для создания английских.
1.  Жмем *New File* сверху справа.
1.  Вводим сверху имя файла в формате дата-название (латиницей, должно совпадать для версий одного поста на разных языках).
1.  Жмем справа кнопку *Meta Data*, заполняем там **Title** (название поста на нужном языке), выбираем язык.
1.  Для английских постов в **Raw Metadata** нужно вставить

    ```yaml
    categories:
      - en
    ```
1.  С помощью редактора заполняем содержимым в формате [Markdown](http://daringfireball.net/projects/markdown/basics).
1.  Жмем **Unpublished**, чтобы пост был опубликован (если не надо пока публиковать, можно оставить неопубликованным).
1.  Жмем справа *Save*, жмем **COMMIT**.

## Работа с остальной частью сайта

Остальная часть сайта (не посты) представлена в виде обычного HTML либо Markdown, работать с которыми тоже можно из [prose](http://prose.io/#CLLKazan/issst-site).
В корне лежит русская версия сайта, в /en/ английская. Каждая страница должна присутствовать и там, и там.

У русских страниц в metadata должно присутствовать:

```yaml
lang: ru
```

У английских:

```yaml
lang: en
categories:
  - en
```

Также в metadata (лучше в начале) должно быть

```yaml
layout: default
title: {<title> страницы}
```

При возникновении проблем рекомендуется обратиться к [документации Jekyll](http://jekyllrb.com/docs/home/).

## Как заливать файлы
1.  Любым ftp клиентом коннектимся на ftp://issst.itis.kpfu.ru.
Данные для входа спросите у кого-нибудь, например, у меня: fsqcds@gmail.com
2.  Заливаете файлы в соответствующие поддиректории issst-site-assets.
3.  Все, ваши файлы доступны по адресам http://issst.itis.kpfu.ru/assets/{путь_к_файлу_относительно_issst-site-assets}. На них можно ссылаться в страничках сайта с помощью относительных путей, например, так (html картинки):

    ```html
    <img src="/assets/images/people/solovyev.jpg" />
    ```
    
    или так (markdown ссылки к pdf)
    
    ```markdown
    [публикация](/assets/pub/article.pdf)
    ```
