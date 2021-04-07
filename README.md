# Minimisation-of-antibiotics-in-patients-with-COVID-19

![newplot](https://user-images.githubusercontent.com/75216349/113827979-8f47e000-978c-11eb-8851-d99ab2e0c7b6.png)

In clinical practice, the prescription of antibiotics requires indications: the presence of a proven or highly probable presence of bacterial flora that causes an infectious process. In the meantime, there is no need to know about it. 

Typical pneumonia (pneumonia) in 95% of cases is caused by a bacterial infection, therefore, antibiotic therapy in case of pneumonia is prescribed in 100% of cases. However, with the advent of coronavirus infection, the balance of etiological factors has changed.

In viral infections, antibiotics are not indicated, because there is no point of application of this group of drugs, however, on the other hand, when the bacterial flora is attached, antimicrobial drugs are indicated, because it has been proven that they improve the prognosis in this category of patients. In the meantime, there is no need to know about it. ”

Thus, there is a circumstance that dictates the doctor to prescribe antibacterial agents if it is impossible to exclude the presence of bacterial flora in patients with viral infections.

To some extent, the solution to the problem of unjustified antibiotic therapy is to study the level of procalcitonin

An increase in the level of procalcitonin in the blood above 0.5 ng / ml indicates the development of a bacterial infection (sensitivity - 80–95%, specificity - 88–93%) !!!

However, the availability of this analysis is a significant limitation of this solution, therefore, there is a need to find a method that would allow determining indications for antibiotic therapy in addition to the level of procalcitonin.




The purpouse: Build a machine learning model that can minimize the number of prescribed antibiotics with zero false negatives
# Availible data:
ВЫПИСНОЙ ЭПИКРИЗ № 170 Находился(ась) в пульмонологическом отделении ГОКБ МР Ф.И.О:*** Дата рождения:02.08.1966 Адрес регистрации:*** Адрес проживания: **Место работы:** Должность: Поступил: 13.01.2021 Выписан: 26.01.2021​

Диагноз клинический: Тяжёлая коронавирусная (ТОРС-КОВ-2 ПЦР+ от 12.01.2021 ) инфекция. Острое вирусное повреждение лёгких, КТ 3 ДН 1 ст.​

Диагноз заключительный клинический: B34.2 / (основной) / Тяжёлая коронавирусная (ТОРС-КОВ-2 ПЦР+ от 12.01.2021) инфекция. Острое вирусное повреждение лёгких, КТ 3 в стадию обратного развития, ДН 0 ст. ИБС: Атеросклеротический кардиослкероз. Атеросклероз аорты, коронарных артерий. АГ 2ст., риск 4. Н 1ст. Сахарный диабет, тип 2, клинико-метаболическая субкомпенсация. МКБ ( оперативное лечение 2019) ХБП С2 ( рСКФ -72 мл/мин/1,73м2). Дискогенная радикулопатия S1 слева, стойкий выраженный болевой синдром. Диабетическая полинейропатия, дистальный тип, с умеренными сенсо-моторными нарушениями. Ожирение 3 ст. (ИМТ - 42 кг/м2)​

Консультации врачей-узких специалистов, консилиумы врачей:​

Консультация невролога 14.01.2021, 20.01.2021 Консультация нейрохирурга 20.01.2021 показаний к экстренному оперативному вмешательству нет​

Результаты инструментальных и аппаратных методов исследования:​

ЭКГ от 13.01.2021 Ритм синусовый, правильный, ЧСС - 93 уд в мин, норм.полож.ЭОС, неспецифические изменения в миокарде нижней стенки ЛЖ МРТ от 19.01.2021 Заключение: МР-картина дегенеративно-дистрофических изменений пояснично-крестцового отдела позвоночника в виде остеохондроза с экструзией диска в Л5-С1 сегменте Результаты лабораторных исследований: Гликемический профиль 14.01.2021: 8 ч. 00 мин. 25.8 ммоль/л ; 12 ч. 00 мин. 24.3 ммоль/л ; 16 ч. 00 мин. 25.5 ммоль/л ; Гликемический профиль 20.01.2021: 8 ч. 00 мин. 9.8 ммоль/л ; 12 ч. 00 мин. 10.3 ммоль/л ; 16 ч. 00 мин. 9.5 ммоль/л ; Гемостазиограмма 14.01.2021: Активированное частичное тромбопластиновое время 22.1 с ; Ratio АЧТВ 0.744 ; Протромбированное время 11.2 с ; Протромбиновый индекс 1.01 ; Международное нормализованное отношение 0.981 ; Фибриноген 8.1 г/л ; Биохимическое исследование крови 14.01.2021: Общий белок 71 г/л ; Мочевина 10.7 ммоль/л ; Креатинин 98.1 мкмоль/л ; C-реактивный белок 41.5 мг/л ; Билирубин общий 10.5 мкмоль/л ; Аспартатаминотрансфераза 27.8 Ед/л ; Аланинаминотрансфераза 54.0 Ед/л ; Натрий 138.7 ммоль/л ; Калий 5.89 ммоль/л ; э\ Прокальцитонин от 14.01.2021 0.14 нг/мл Биохимическое исследование крови 15.01.2021 Глюкоза - 22,1 ммоль/л Общий анализ крови 14.01.2021: WBC (Лейкоциты) 9.1 109/l ; RBC (Эритроциты) 4.09 1012/l ; HGB (Гемоглобин) 129 g/l ; PLT (тромбоциты) 495 10*9/l ; СОЭ 35 мм/ч ; Нейтрофилы палочкоядерные 3 % ; Нейтрофилы сегментоядерные 68 % ; Лимфоциты 26 % ; Моноциты 3 % ; \С у м м а к л е т о к: 100 ;​

Состояние при выписке: относительно удовлетворительное. При выписке сатурация крови кислородом при дыхании атмосферным воздухом - 97%, ЧД 18 в мин. уровень лейкоцитов более 3 тыс. на мл., не лихорадит более 3 дней без жаропонижающих. Уровень СРБ менее 2х норм​

Проведенное лечение: гепарин, пантопрозол, ацецезон, гликлазид, метформин, лизиноприл, метопролол, индапамид, эуфиллин, новокаин, димедрол, вит группы В, ксефокам, толперизон, карбомазепин, кетаролак, зопиклон, пентоксифиллин, трамадол, мелоксикам, ФТЛ​

Рекомендации:Наблюдение участкового терапевта, эндокринолога, невролога по месту жительства (Д3) Избегать переохлаждений, витаминно-минеральный комплекс Снижение употребления поваренной соли менее 5грамм в сутки, животных жиров, рафинированных углеводов. Повышение употребления овощей , омега-3 ненасышеные ЖК, умеренные аэробные физические нагрузки Контроль гликированного гемоглобина Целевой уровень ЛПНП - ниже 1,8 ммоль/л Ривароксабан 10 мг 1 раз в день ( 45 дней), при невозможности - аспикард 75 мг после обеда ( не менее 3 месяцев) Ацетилцистеин 1,2 в день - 45 дней Гликлазид 60мг 1 табл. утром Метформин 1000мг 2 раза в день Лизиноприл/гидрохлортиазид 10/12,5мг утром Метопролол 25 мг 2 раза в день Невролог: 1) Дексамин 2,0 в/м № 5 2) Нимесулид 100 мг 2 раза в день ( утро, вечер) при необходимости 3) Мидокалм 150 мг по 1 табл 3 раза в день - 14 дней 4) Боривит 2,0 в/м № 10​

Using 
-Glob​

-Os​

-Regex​

-String​

-NLTK
had been done info extraction




The procalcitonin level over 0.4 ng / ml is selected as the threshold for the indication of AB therapy
Target:
1 - AB are shown;
0 - AB not shown
