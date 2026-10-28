# Лабораторна робота №3. Візуалізація даних (Tableau)

**Виконав:** Стьоба Вадим Костянтинович, група ІП-35  
**Дисципліна:** Юніт-економіка та продуктові метрики

## Дашборд на Tableau Public

https://public.tableau.com/app/profile/vadim.stoba/viz/ProductOverviewDashboardStobaIP-35/Dashboard1

Опцію «Show Sheets» увімкнено: усі аркуші доступні як вкладки.

## Резервна копія

`Product_Overview_Dashboard_Stoba_IP-35.twbx` – Tableau Packaged Workbook з вшитими даними (registrations, payments, sessions_daily, country_info_dict). Відкривається в Tableau Desktop або Tableau Public Desktop.

## Що всередині

- **Модель даних:** relationships навколо `registrations` (payments і sessions_daily за `user_id`, country_info_dict за `country_code`).
- **Acquisition:** New Users – `COUNTD(user_id)` за датою реєстрації, щоденна динаміка.
- **Engagement:** Active Users / DAU – `COUNTD(user_id)` за день; Avg Time in App – `AVG` хвилин на користувача за день.
- **Monetization:** Revenue – `SUM(amount_usd)`; Avg Check – `AVG(amount_usd)`; топ-5 країн і платформи.
- **Інтерактивність:** період задається параметрами Start Date / End Date; фільтри країни та платформи застосовано як «All Using This Data Source».

`sessions.csv` (1,5 млн рядків) попередньо агреговано до рівня «користувач – день», щоб вкластися в ліміт завантаження веб-редактора.

## Скриншоти

![Дашборд](screenshots/dashboard_top.jpg)
![Нижня частина](screenshots/dashboard_bottom.jpg)
![Фільтр Ukraine](screenshots/filter_ukraine.jpg)
![Модель даних](screenshots/data_model.jpg)
