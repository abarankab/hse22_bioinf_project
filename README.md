# hse22_bioinf_project

Ссылка на colab: https://colab.research.google.com/drive/17OhDA0wb68TpCfIs54p8LK3ojRkNcfhA?usp=sharing

## Результаты по zhunt

| Название организма              |   Число последовательностей |   Общая длина последовательностей |   Число аннотированных генов |   % аннотированных генов |   Участков z-dna с score > 500 |   Общая длина z-dna с score > 500 |
|:--------------------------------|----------------------------:|----------------------------------:|-----------------------------:|-------------------------:|-------------------------------:|----------------------------------:|
| Leuconostoc carnosum            |                           3 |                           1701333 |                         1732 |                    89.16 |                           2236 |                             22074 |
| Leuconostoc citreum             |                           2 |                           1791608 |                         1818 |                    84.66 |                           4447 |                             43406 |
| Leuconostoc lactis              |                           2 |                           1903250 |                         1941 |                    79.7  |                           2828 |                             27474 |
| Leuconostoc mesenteroides       |                           3 |                           2058732 |                         2082 |                    73.68 |                           2069 |                             20280 |
| Leuconostoc pseudomesenteroides |                           1 |                           2114657 |                         2115 |                    71.73 |                           2794 |                             27126 |

## Результаты по кластерам

Всего было получено 1936 кластеров.

### Гистограммы

![download](https://user-images.githubusercontent.com/12930866/173673591-0ded79dc-c6e4-4f93-8bf2-82ba56ede574.png)

![download](https://user-images.githubusercontent.com/12930866/173673604-9846c747-a968-4554-b8aa-bdb4786d5215.png)

### Таблица по выбранным кластерам

|   Номер кластера | Функция                   |   Число генов |   Число z-dna в промотерах |   Число z-dna в генах |   Средний z-dna score |
|-----------------:|:--------------------------|--------------:|---------------------------:|----------------------:|----------------------:|
|                0 | 30S ribosomal protein S10 |             5 |                          5 |                     3 |              2836.89  |
|                1 | 50S ribosomal protein L34 |             5 |                          5 |                     5 |               948.834 |
|                2 | 30S ribosomal protein S9  |             5 |                          5 |                     1 |               753.541 |
|                3 | 50S ribosomal protein L14 |             5 |                          5 |                     5 |               883.576 |
|                4 | 50S ribosomal protein L16 |             5 |                          5 |                     5 |               712.187 |

По числу z-dna в промотерах и генах можно понять, что, например, у 0 и 2 кластера все участки z-dna находятся рядом с геном, но не все находятся прямо в нем. В остальных кластерах участки также находятся непосредственно в самом гене. Я не понял как более удобно описать расположение z-dna относительно гена в табличке, поэтому сделал так.

### Выравнивания 

Выравнивания будут в папке alignments. Я сделал их с помощью MUSCLE.

### Визуализации расположения

![download](https://user-images.githubusercontent.com/12930866/173673991-d7afaf72-c84e-424b-9a32-e726306fb8ad.png)

![download](https://user-images.githubusercontent.com/12930866/173674009-c8ed1247-1689-40f0-8ef2-453fd0de9ef9.png)

![download](https://user-images.githubusercontent.com/12930866/173674026-c693701c-dd1d-4e8b-aaf5-41f8e74561ce.png)

![download](https://user-images.githubusercontent.com/12930866/173674047-2f9fcdd5-8cbf-46dc-b284-1d52775ee9d9.png)

![download](https://user-images.githubusercontent.com/12930866/173674067-4982f988-26e5-4643-9fac-508209f577d2.png)

## Бонус

Предсказано G-квадруплексов для Leuconostoc carnosum: 5, 0 на промотерах

Предсказано G-квадруплексов для Leuconostoc citreum: 25, 1 на промотерах

Предсказано G-квадруплексов для Leuconostoc lactis: 3, 1 на промотерах

Предсказано G-квадруплексов для Leuconostoc mesenteroides: 5, 2 на промотерах

Предсказано G-квадруплексов для Leuconostoc pseudomesenteroides: 5, 1 на промотерах

Пример предсказания для Leuconostoc carnosum:

| chr                                                                           |   Start |     End | ID                                                                                                |   length | strand   | seq                                       |
|:------------------------------------------------------------------------------|--------:|--------:|:--------------------------------------------------------------------------------------------------|---------:|:---------|:------------------------------------------|
| NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome |  731704 |  731734 | NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome_731704_731734_rev   |       30 | -        | CCCAAGTTCAACACCCGCCCAGCTTTACCC            |
| NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome |  871461 |  871502 | NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome_871461_871502_rev   |       41 | -        | CCCAATCACGTCCCCACAAGACACCCATCGTACCATCTCCC |
| NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome | 1153352 | 1153390 | NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome_1153352_1153390_rev |       38 | -        | CCCTTGTAGGTACGTCCCAATTCCCCAGTATCTGTCCC    |
| NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome | 1527864 | 1527902 | NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome_1527864_1527902_for |       38 | +        | GGGAAAACTTTGGGCGTTATTGGTTTGGGAAATGTGGG    |
| NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome | 1531238 | 1531260 | NZ_CP042374.1 Leuconostoc carnosum strain CBA3620 chromosome, complete genome_1531238_1531260_for |       22 | +        | GGGCTGTTGGGATGGGTCTGGG                    |

Было найдено 40 кластеров где на одном из генов есть G-квадруплекс. И всего два где на хотя бы двух генах есть G-квадруплекс. Не было случаев чтобы G-квадруплексов было больше двух.

Приведу визуализацию двух примеров где есть два G-квадруплекса.

![download](https://user-images.githubusercontent.com/12930866/173684759-ef8686e7-9e77-4b9e-aadc-480318cb5648.png)

![download](https://user-images.githubusercontent.com/12930866/173684781-18c2c39e-3080-42b4-8130-62c6accec7f5.png)

Был найден кластер где есть два квадруплекса возле промотера, вот его визуализация:

![download](https://user-images.githubusercontent.com/12930866/173685638-da6fc24e-a69a-4aa8-a08f-bf4e17329a57.png)
