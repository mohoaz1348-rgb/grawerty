# Grawerty

Grawerty is a layout for comfortable typing in English. It was originally designed for a standard keyboard, but can be adapted for other keyboard types. It uses Angle Mod: `c` is the index finger, `x` is the middle finger, and `z` is the ring finger.

![grawerty](./img/grawerty.png)

- White - Characters retain their position (relative to Qwerty)
- Green (`t`, `h`, `y` - 15.4%) - The letter remains on the same finger of the same hand
- Blue (`l`, `m`, `f`, `e` - 20.4%) - The letter retains its finger but changes hands
- Yellow (9 letters - 22.5%) - The letter changes fingers but retains its hand
- Red (`n`, `a` - 14.7%) - The letter changes both fingers and hands

Eighteen letters, with a combined frequency of 73%, changed their positions, of which three letters, with a combined frequency of 15.4%, retained both their finger and hand positions. This means the layout has changed relative to Qwerty by 58%. I consider this a nice additional bonus, although not the main one (see comparison with other layouts).

## The reason for creating Grawerty

The first alternative layout I switched to was Graphite, and it truly was much nicer than Qwerty - learning was faster and more comfortable. Within a month, I reached 50 wpm, and my speed kept increasing. But I noticed some inconveniences that were critical for me:

- I don't like rolling movements involving the pinky and middle fingers, and there are a lot of them in Graphite: `nd`, `nt`, `io`, `ai`, and `ia`.
- After Qwerty, placing the `t` on a finger other than the index finger was very unusual, but even without reference to Qwerty, I personally find placing the `t` on the index finger very comfortable and natural. Incidentally, the creator of Graphite places the `t` on the index finger in his subsequent layouts.
- I don't like the placement of the `m` in Graphite because Typing `rm`, `rms`, `mb`, `lm` becomes awkward for me.
- `br`, `ui` are uncomfortable, so when creating the layout, I paid close attention to the half-scissors, especially on the pinky and ring fingers.
- I don't like weak redirections and try to avoid them. There are significantly fewer of them in Graphite than in the standard layout, but they can be reduced even more.

## Layout requirements

- eliminate the shortcomings of Graphite without introducing new shortcomings
- the number of redirections should not increase significantly compared to Graphite
- significantly reduce the number of weak redirections
- I like that only 6 letters changed hands in Graphite, so leave them that way – no changes
- SFB should not exceed the SFB of the Dvorak layout
- SFB should be comfortable to type; SFBs on the pinky are unacceptable, including SFB(0u) (repeating a single letter)
- almost zero scissors (except when the index finger is at the bottom and the middle or ring finger is at the top)
- almost zero half-scissors on the pinky/ring finger
- the placement of `c` and `v` matches Qwerty and Graphite (Angle Mod)
- preserve the characters placement of the standard layout whenever possible. If a change is made, it should provide a significant benefit

## Results

I managed to meet all the requirements, but I couldn't create a layout that would satisfy them and still be stressful for my pinkies (I don't mind the stress on my pinkies, as long as the letters on my pinkies don't form awkward combinations). Therefore, I created a layout that places low stress on my pinkies. Although on a standard keyboard, there's plenty of work for my little fingers. As you can see, Grawerty has a lot in common with both Qwerty and Graphite, hence the name Grawerty.

The arrangement of the letters `u`, `i`, and `o` was the same as in the standard layout not to maintain similarity, but because this arrangement best meets the requirements of the new layout. Surprise. The same applies to the letter `c` – it retained its position, in part because moving it to other fingers, while reducing sfb, also increases other inconvenient combinations – weak redirects, half-scissors, and pinky/middle finger rolls (which I don't like).

## Сравнение с графитом и другими раскладками

![Grawerty](./img/grawerty_oxey.png)

### Trigrams

1. The overall number of redirections increased by only 0.8% compared to Graphite – that's fine with me.
2. The number of weak redirections decreased by 0.3% and became very insignificant – 0.1%.
3. The number of rolls decreased slightly, but I don't really pay attention to their number, as these rolls tend to include scissors and other awkward combinations. I just make sure there aren't many more outward rolls than inward ones.

### Bigrams

SFB – in my opinion, this parameter is overly demonized and optimized at all costs, but this also creates other inconvenient combinations that modern analyzers don't catch because their bigram analysis is incomplete. This can be verified by adding up the values ​​of all analyzed bigrams: sfb + lsb + scissors < 5%. Where are the rest?

Итак, SFB - 2.55%. В два с половиной раза больше, чем у графита! Тут все разворачиваются и идут по своим делам - т.к. сразу считают, что это плохая раскладка. Но на самом деле SFB ещё больше, т.к. анализатор не учел повторы одной буквы, которые для английского языка составляют 2.3%.

So, the SFB is 2.55%. Two and a half times higher than Graphite's SFB! Everyone turns around and goes about their business, immediately assuming this is a bad layout. But in reality, the SFB is even higher, because the analyzer didn't account for repeats of one letter, which account for 2.3%.

Now, Grawerty has 4.85%, while Graphite has 3.3%. Not that big of a difference, right? 50% more than Graphite. This extra percentage is quite comfortable to type, as it's concentrated in just a few bigrams on the index and middle fingers. `rs`, `ie` are comfortable, `ct` is less comfortable, `e` is awkward, `up`, `pu`, `fu`, `dg`, `dv` are easy to type using the index and middle fingers - this is quite familiar to Qwerty users.

Scissors are almost the same as in Graphite.

LSB - 2.5%. Graphite - 1.4%. Acceptable for me.

This is where bigram analysis ends for many analyzers, although relatively little has been analyzed. To fill this gap, I created my own bigram analyzer - [ABA](https://github.com/mohoaz1348-rgb/layout_bigrams_analyzer) - All Bigrams Analyzer. It has a completely different concept from other analyzers, so to understand what it analyzes and how, read the readme file.

Here are the results in percentages for some layouts:  
`-3` are the most inconvenient combinations, `3` are the most convenient

![compare_table](./img/compare_table.png)

It's clear that, according to my own preference matrix, Grawerty is the most convenient layout (for me). You can customize this matrix to suit your needs and see which layout is most comfortable. However, this is a labor-intensive process and requires self-observation and an open mind.

#### A slight digression from the topic

The table shows that Graphite still holds a fairly high position—the only thing better for me is Comet, from the creator of Graphite, who likes Comet more than Graphite. Northstar is on par with Graphite, and Gallium is slightly lower. Canary is a good layout, but it doesn't suit me because it has too many redirects, but at least it has fewer weak redirects than Graphite.

Among layouts with a large number of redirects, Workman wins, with a few inconvenient bigrams and many convenient ones. Colemak-dh was a surprise, losing to Colemak.

It is also clear that Angle Mod provides an advantage over the standard mode for Qwerty, Colemak, and Workman.

## Мой опыт использования английских раскладок

Год назад я решил освоить слепой метод печати для Qwerty. Три недели занимался на тренажере, затем пришел на [клавогонки](https://klavogonki.ru/) и начал тут набирать скорость. С результатами можно ознакомиться [здесь](https://klavogonki.ru/u/#/808252/stats/voc-5539/?fromDate=2025-02-26&toDate=2026-01-22&grouping=day&indicator=speed).

За два месяца и три недели я достиг максимальной скорости 287 знаков в минуту и она отказывалась дальше расти. При печати довольно быстро наступало утомление - особенно на левой руке (сейчас я понимаю, что так происходило из-за большого количества перенаправлений, особенно слабых). Тренироваться было не в кайф. Начал присматриваться к альтернативным английским раскладкам - остановился на графите и начал его тренировать.

За месяц на графите я достиг максимума 250 символов и скорость не переставая росла. Со статистикой можно ознакомиться [здесь](https://klavogonki.ru/u/#/817942/stats/voc-5539/?fromDate=2025-05-04&toDate=2026-01-22&grouping=day&indicator=speed). Графит это только начало графика, остальное Grawerty.

Т.е. на графите прогресс был заметно быстрее и печатать гораздо приятнее было. Но для меня графит не совсем подходил. Поэтому, после того как я допилил и окончательно протестировал русскую раскладку [Статикa](https://github.com/mohoaz1348-rgb/statica), я приступил к созданию английском раскладки. Т.к. я уже понимал что мне нужно от раскладки, то сделал её довольно быстро и за два месяца достиг 350 символов в минуту. За это время изменили своё пложение буквы `r`, `l`, `f`, `y`, `k` и раскладка обрела окончательный вид.

Прогресс на Grawerty шел ещё быстрее, чем на графите. Прирост скорости по сравнению с Qwerty уже составил 22%, хотя тренировался меньше на две недели и в процессе этих тренировок раскладка менялась. Так что могу с уверенностью сказать, что альтернативные раскладки, особенно хорошие, дают существенный прирост как в скорости, так и в комфорте набора.

### Что мне особенно нравится в раскладе

- блок wnst/blrd. В этом блоке сконцентрированы самые частые согласные, которые легко доступны и образуют много удобных и мало неудобных сочетаний друг с другом
- блок hea;/uioj. Нравится по той же причине, что и левый блок, но уже меньше, т.к `j` немного портит статистику, неудобными сочетаниями с некоторыми гласными буквами
- незначительное использование мизинцев всё-таки добавляет комфорта, хотя я и не стремился специально снизить на них нагрузку
- большое сходство со стандартной раскладкой при использовании наиболее частых шорткатов
- пунктуация совпадает с Qwerty (с графитом я тоже использовал стандартную пунктуацию)

### Что мне не нравится в раскладке

- левый указательный палец двигается довольно интенсивно и скачет туда сюда, это не сильно сказывается на удобстве, но может сказаться на высоких скоростях набора. Хотя этот показатель всё равно намного лучше, чем у Qwerty. Неудобство вызывает скипграмма `c_m`.
- `e,` - не очень удобная sfb для меня. При желании можно поменять местами `,` и `;`.
- `phy` - удобнее чем в графите, но всё равно требует усилий
- `k` - расположение не самое оптимальное, так как образует много сочетаний с гласными буквами и хотя не доставляет неудобств, но вызывает перепробег указательного пальца. Но не советую менять местами `k` и `;`, т.к. это вызовет значительный рост слабых перенаправлений

### Кое-какие замечания

- `m` - может показаться, что эта довольно частая буква труднодоступна. Место, действительно, не самое удобное, но гораздо важнее, чтобы буква не вызывала неудобных сочетаний. Сочетания `rm`, `mb`, `lm`, `ms` - либо удобны, либо нейтральны. Они все равно удобнее, чем в графите, по крайней мере для меня. Если же буква `m` участвует в биграммах, для набора которых используются разные руки, то её расположение, вообще, не вызывает проблем. На практике, с этой буквой я не испытываю трудностей.

## Установка

### Windows

Для создания раскладки существует программа [Microsoft Keyboard Layout Creator](https://www.microsoft.com/en-us/download/details.aspx?id=102134). Видео по созданию раскладки - https://www.youtube.com/watch?v=HMDSJfwi0Kc.

Уже готовый klc-файл с раскладкой и инсталлятор (сделаны мной) - [здесь](./windows/Grawerty10.7z).
Klc-файл можно открыть в программе и подредактировать, а затем из него создать инсталлятор. После инсталляции раскладки лучше перезагрузиться. Даже если вы не будете самостоятельно создавать раскладку - видео все-равно посмотрите, т.к. там указаны и другие шаги, необходимые для использования раскладки.

Для удаления раскладки нужно запустить инсталлятор повторно.

#### Предупреждение:

Инсталлятор создавался и проверялся на Windows 10.

### Mac

### Linux

Добавить содержимое [файла](./Linux/xkb/symbols/us) в файл - `/usr/share/X11/xkb/symbols/us`.

#### Предупреждение:

При обновлении системы `/usr/share/X11/xkb/symbols/us` может обновиться и нужно будет устанавливать раскладку снова.
