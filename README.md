ruHaskell
=========

Главный сайт русскоязычного сообщества Haskell-разработчиков. 

Наше желание - использовать этот прекрасный язык, а не просто разговаривать о нём.<br/>
Наше стремление - объединить всех хаскелистов, говорящих по-русски.<br/>
Наша цель - увеличить долю использования Haskell в России.

### Зачем

Главной ценностью нашего сайта являются статьи. Я уверен, что каждому Haskell-энтузиасту есть что рассказать коллегам, но наши блоги разбросаны по просторам интернета, а кроме того, не всем хочется строить собственное блоговое пространство. Поэтому наш сайт представляет собой единое место обмена опытом, где каждый сможет рассказать обо всём, так или иначе связанном с разработкой на Haskell.

### Темы

Принимаются материалы, так или иначе связанные с разработкой на Haskell. Это может быть что угодно:

- Разжёвывание фундаментальной теории. Например, что-нибудь о категориях и иже с ними.
- Рассмотрение любых аспектов языка, от Hello World до монадических глубин.
- Рассказ об инструментах, связанных с Haskell. И это не только Yesod. ;-)
- Готовые практические рецепты. Что называется, копи-паст - и вперёд!
- Истории успеха или неудачи, связанные с практической разработкой на Haskell.
- Пиар программного решения, реализованного с помощью Haskell.

Причём технический уровень статей может быть рассчитан на любых читателей, от "нулевых" новичков до экспертов.

### Авторам

Статьи принимаются в формате `Markdown`, рекомендуется использовать расширение `.md`.

#### Информация о статье

В начале каждой статьи должен присутствовать информационный блок следующего вида:

```
---
author:         Денис Шевченко
title:          Yesod: знакомство
tags:           Yesod, веб
description:    Yesod - это мощный веб-фреймворк, написанный на языке Haskell.
---
```

где:

- `author` - имя автора статьи,
- `title` - название статьи,
- `tags` - один или более тематических тегов, перечисленных через запятую,
- `description` - краткое описание статьи, необходимое для обновлений в RSS.

Кроме того, существует опциональное поле `hrefToOriginal`. Если оригинал публикуемой вами статьи находится на стороннем ресурсе, просто допишите поле `hrefToOriginal` к вышеупомянутым полям:

```
hrefToOriginal: https://www.fpcomplete.com/user/astynax/basics/pine-tree
```

В результате этого в верхней правой части статьи будет размещена ссылка на оригинал.

**Внимание!** Если автором оригинала публикуемой вами статьи являетесь _не вы_ - убедитесь в том, что автор согласен на публикацию его статьи в рамках нашего ресурса.

#### Правила именования

Имя файла статьи должно быть сформировано следующим образом:

```
гггг-мм-дд-краткое-имя-статьи.md
```

Например:

```
2014-12-27-yesod-raw-deploy.md
```

URL этой статьи станет таким:

```
/posts/2014/12/27/yesod-raw-deploy.html
```

Это позволит отфильтровать статьи по дате публикации. Причём если номер месяца или дня меньше 10, то его необходимо начинать с `0`. Например, публикация от 1 мая должна быть названа так:

```
2014-05-01-yesod-raw-deploy.md
```

#### Расположение

Все Markdown-статьи хранятся в ветке `master`. Иерархически они располагаются в каталоге `posts`, но не в корне, а обязательно в своём тематическом подкаталоге. Имя подкаталога соответствует названию категории. Например, все статьи из категории `web` располагаются в каталоге `posts/web/`. Разумеется, поскольку имя каталога участвует в формировании базового URL статьи, оно должно быть английским.

Посколько Git не любит пустые каталоги, тематические подкаталоги будут создаваться по мере написания статей.

### Локальная сборка

Вы можете собрать сайт локально. Подразумевается, что [Haskell Platform](https://www.haskell.org/platform/) у вас уже установлена. Итак:

```bash
$ git clone git@github.com:denisshevchenko/ruhaskell.git
$ cd ruhaskell
$ cabal sandbox init
$ cabal install --only-dependencies
$ ./just_build.sh
```

После этого откройте в браузере страницу `ruhaskell/_site/index.html`.

### Устав нашего монастыря

Как известно, в чужой монастырь со своим уставом не ходят, а потому вот устав нашего монастыря.

Трём вещам объявляется бой:

1. **оскорбления в любой форме**,
2. **явный оффтоп**,
3. **спам**.

Статьи и/или комментарии, содержащие первое, второе или третье, будут удалены. Вот и весь наш устав.

### Обратная связь

Вопросы? Предложения? Критика? Вы можете задать их в нашем [чате](https://gitter.im/denisshevchenko/haskell), на форуме (скоро будет), в [группе на Google+](https://plus.google.com/communities/117343381540538069054) или же написать [лично мне](mailto:me@dshevchenko.biz).
