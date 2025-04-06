# Android News App

Android приложение за четене на новини, изградено с Java 17 и Gradle 7.5, използвайки NewsData.io API.

---

## Технологии
- **Език**: Java 17
- **Система за билдване**: Gradle 7.5
- **HTTP клиент**: Retrofit
- **Зареждане на изображения**: Picasso
- **API**: [NewsData.io](https://newsdata.io/)
- **Запазване на данни**:
  - Internal Storage (saved.txt файл) за запазени новини
  - SharedPreferences за потребителски настройки

---

## Основни функции

- **MainActivity**: Показва новините в card-based оформление чрез RecyclerView
- **DetailsActivity**: Показва подробности за избрана новина
- **SavedActivity**: Показва списък със запазени новини
- **SettingsActivity + SettingsFragment**: Настройки на приложението чрез PreferenceScreen

---

## Навигация

- **Explicit Intents**: За навигация между екрани в приложението
- **Implicit Intents**: За отваряне на външни линкове в браузър

---

## Съхранение на данни

- **Запазване на новини**: 
  - Статиите се сериализират като JSON стринг и се записват във файл (`saved.txt`) в **Internal Storage**.
- **Настройки на потребителя**:
  - Съхраняват се с **SharedPreferences** (например избор на държава/регион и активиране/деактивиране на известия).

---

## Работа без интернет

- Използва `ConnectivityManager`, за да провери състоянието на интернет връзката.
- Ако няма връзка, се показва **Toast** съобщение и новините не се зареждат.
- Потребителят все пак има достъп до запазените новини и настройките.

---

## Допълнителни функции

- **Swipe to Refresh**:
  - Дръпване надолу за презареждане на новините в MainActivity и обновяване на списъка в SavedActivity.

---

## 📄 Документация

- [ECM2425 - Coursework.pdf](./ECM2425%20-%20Coursework.pdf) — Описание на курсовата работа.

---
