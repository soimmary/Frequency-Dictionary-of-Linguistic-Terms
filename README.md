# Частотный словарь лингвистических терминов
Это проект, выполненный в рамках курсовой работы Марии Бочаровой, студентки 2 курса 191 группы Школы лингвистики НИУ ВШЭ.


## Цель исследования
Целью исследования является составление частотного словаря лингвистических терминов на базе созданного корпуса лингвистических статей и диссертаций. В этой работе будет продемонстрирована динамика и частотность употребления как отдельных лексем, так и коллокаций (n-грамм). 

## Задачи исследовани
1. Составить корпус текстов лингвистической тематики:

В папке _**crawlers**_ назодятся скрипты программ, собирающих необходимые данные для пополнения корпуса.
_**texts_by_year.py**_ – сортируем тексты, разбиваем их на предложения и лемматизируем, создаем один файл со всеми текстами и обучаем на нем модель word2vec (https://drive.google.com/drive/u/0/folders/17Bo0P0vgAUiMKySRmfBXHnHBrgJSFGJx). 

2. Определить оптимальный статистический подход и извлечь однословные термины и n-граммы;

_**freq_words_filter.py**_ – извлекаем однословные термины, применяем различные фильтры (stop-words, Natasha, contrast dictionary). 

_**find_most_similar.py**_ – с помощью натренированное модели word2vec ищем ближайшие по векторам к терминам слова. 

_**ngram_analysis.py**_ – создаем списки частотных n-грамм, фильтруем их, создаем таблицы, содержащие информацию о частотности термина (ipm) на всем корпусе и в определенные временной промежуток.

3. Определить метод подсчета статистических данных о частоте встречаемости терминов;

_**statistics.py**_ – подсчет метрик Jiulland's _D_, R, DP.

4. Составить списоки частотных терминов и коллокаций и представить динамику их употребления;

В папках _**unigrams, bigrams, trigrams, fourgrams, fivegrams**_ содержится вся статистическая информация о лингвистических терминах. Частотные данные представлены в двух форматах: сортированные по частоте (ipm) на всем корпусе и по алфавиту. 

5. Сделать выводы о динамике использования отдельных терминов. 


## Источники пополнения корпуса
#### Научные журналы:
1. «Русская речь»
2. «Русский язык в научном освещении»
3. «Лингвистическое источниковедение и история русского языка»
4. «Acta Linguistica Petropolitana»
5. «Лингвистика и методика преподавания иностранных языков»
6. «Русский язык за рубежом»
7. «Русский язык в школе»
8. «Вопросы ономастики»
9. «Вопросы языкознания»
10. «Советская тюркология», «Российская тюркология»
11. «Социолингвистика»
12. «Вопросы психолингвистики»
13. «Урало-алтайские исследования»
#### Другие материалы:
15. Материалы конференций «Диалог»
17. «Русский филологический портал»
18. статьи, опубликованные на сайте «Грамота.ру»

## Метаинформация
 Таблица, содержащая метаинформацию источников, вошедших в корпус:
 https://github.com/soimmary/CourseWork/blob/main/metadata.csv

## Над проектом работали:
М. В. Бочарова: mvbocharova@edu.hse.ru
#### Академический руководитель:
Б. В. Орехов: nevmenandr@gmail.com
