# redamage

Занимаемся моделированием стендового эксперимента на ресурсные испытания механизации крыла.

## Описание эксперимента

Есть полётный профиль нагрузок на закрылок (Px(t), Py(t), Mz(t)). Он получен пересчётом из
испытаний аналогичных самолётов, из аэродинамических расчётов, из эксперимента и т.п. Эти три силы
приводят к одной силе, приложенной в выбранном направлении закрылку в какой-то фиксированной точке.

Самая большая нагрузка -- на посадке, поэтому берут точку и направление силы с посадки, и
к этой фиксированной точке в этом фиксированном направлении прикладывают нагрузку во всём эксперименте.

На других режимах полёта прикладывают нагрузку так, чтобы сохранилась повреждаемость в выбранных
критических зонах. Потом, когда где-то треснуло, пересчитывают на соответствующий узел
повреждаемость из эксперимента и сравнивают с оценками ресурса.

Погрешности:
1. Общая методическая из-за сведения распределённых сил к одной сосредоченной.
2. При движении закрылка считается, что направление действующей силы в эксперименте не меняется.
В реальности же это направление значительно меняется.
3. Имеется различие в динамических характеристиках нагружающих приводов и приводов закрылка. Нагрузки
на закрылок и положение закрылка синхронизируют. Есть подозрение, что различие в характеристиках приводов
добавляет лишние циклы при страгивании привода закрылка. Что сказывается на повреждаемости в эксперименте.

## Цель

Валидация стендового эксперимента. Поскольку трудно предсказать, в каких узлах повреждаемость
в эксперименте завышена, то так же трудно утверждать, что эксперимент воспроизводит должным образом
полётные условия. Получается, что можно разрушить образец до достижения нужных повреждаемостей в
критических зонах, интересующих экспериментаторов.

## Задача

Построить модель стендового эксперимента для расчёта повреждаемости во всех точках конструкции и
последующей валидации схемы нагружения.
