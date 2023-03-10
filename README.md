# hse_hw2_chip

## Colab
https://colab.research.google.com/drive/1QKDItTk2hQmJdzIvFWVocu2xfEExr5ul?usp=sharing

## Выбранные данные 

| **Что** | **Какой** | **Комментарий** |
| ------------- | ------------- |--------------------|
| Клеточная линия | A549 | Раковые клетки эпителия легких 58-летнего мужчины с Кавказа ![image](https://user-images.githubusercontent.com/93095449/157491921-fea51ecb-a342-49f2-b19a-384f444d7fa2.png) |
| Гистоновая метка | H3K27ac | Ацетилированный лизин в 27 положении гистона H3. Ассоциируется с высокой активностью транскрипции |
| Реплики 1 и 2, Контроль | ENCFF195ZFO, ENCFF734JYK, ENCFF151SVH | ZFO, JYK и SVH |

## Выдача FastQC

| **ZFO** | **JYK** | **SVH** |
| ------------- | ------------- |--------------------|
| ![image](https://user-images.githubusercontent.com/93095449/157494530-3897a96a-6f5d-4499-9db3-e4614b3af03e.png) | ![image](https://user-images.githubusercontent.com/93095449/157495668-d3f07305-4ae4-44fc-8239-b88288eccee7.png) | ![image](https://user-images.githubusercontent.com/93095449/157496306-46b72bd4-bee4-4e8e-8ab5-f95a39cb40cb.png) |
| ![image](https://user-images.githubusercontent.com/93095449/157494642-dbabcdf0-a2b1-456f-a06e-6fbc7ec07eb3.png) | ![image](https://user-images.githubusercontent.com/93095449/157496166-2250fc8b-e86d-40e2-9f61-1b2f20bc8657.png) | ![image](https://user-images.githubusercontent.com/93095449/157496377-fdbae06d-3693-4b17-9151-8784ba7409a4.png) |
| ![image](https://user-images.githubusercontent.com/93095449/157494746-de7dda1c-668e-4743-94c7-8e281a54ea38.png) | ![image](https://user-images.githubusercontent.com/93095449/157496224-279df110-6025-450f-8219-5cf06ef98d5e.png) | ![image](https://user-images.githubusercontent.com/93095449/157496439-ace6b7df-086e-4386-b203-7adc027e3fe1.png) |

## Результаты выравнивания

|  | **ZFO** | **JYK** | **SVH** |
| ------------- | ------------- |--------------------| ---- |
| Всего ридов | 109131346 | 88120815 | 64750538 |
| Не выровнено | 94077115 (86.21%) | 76904496 (87.27%) | 53995376 (83.39%) |
| Выровнено 1 раз | 4339598 (3.98%) | 3340751 (3.79%) | 2941610 (4.54%) |
| Выровнено больше 1 раза | 10714633 (9.82%) | 7875568 (8.94%) | 7813552 (12.07%) |

Общая длина референснового генома человека в сборке hg38 составляет 3,298,912,062 пар оснований (если без N, то 3,137,300,923 пар оснований). Длина 14-ой хромосомы в этой же сборке - 107,043,718 пар оснований, что составляет примерно 3.24% от всего генома. 

## Сравнение результатов

|  | **ZFO** | **JYK** |
| ------------- | ------------- |--------------------|
| Пересечение **всех** пиков с файлом из ENCODE | <img width="566" alt="image" src="https://user-images.githubusercontent.com/93095449/157662707-5a2355c1-1855-4e9f-814d-8601e161a3b3.png"> | ![image](https://user-images.githubusercontent.com/93095449/157662807-c50b4b89-6fe3-40de-a0b2-b8b80ce19d2b.png) |
| Пересечение файла из ENCODE со **всеми** пиками | ![image](https://user-images.githubusercontent.com/93095449/157662908-318771d7-dede-47d0-90e1-26a36a187a15.png) | ![image](https://user-images.githubusercontent.com/93095449/157662967-ccb52aec-ed07-48e8-812f-f4ae8628046f.png) |
| Пересечение пиков из **уникальных** ридов с файлом из ENCODE | ![image](https://user-images.githubusercontent.com/93095449/157663204-4ab0b0bd-4208-47f3-abcb-bb27c02bbd03.png) | ![image](https://user-images.githubusercontent.com/93095449/157663269-1d5777fc-de6a-4468-aa8f-bdba785f5f64.png) |
| Пересечение файла из ENCODE с пиками из **уникальных** ридов | ![image](https://user-images.githubusercontent.com/93095449/157663331-ab9706b7-6aba-4dfd-b2bd-74142f4d33ad.png) | ![image](https://user-images.githubusercontent.com/93095449/157663387-261c5218-05f2-48f1-8082-c4d0305a6832.png) |
