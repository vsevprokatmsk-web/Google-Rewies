# Vsevprokat Google Reviews

This repository collects visible Google Maps reviews for Vsevprokat once a week with GitHub Actions and Puppeteer.

## Location

- Company: Vsevprokat
- Website: https://vsevprokat.by/
- Address: Минск, Кабушкина 94/2
- Google reviews: https://www.google.com/maps/place/Vsevprokat/@53.8564378,27.6306567,17z/data=!3m1!4b1!4m18!1m9!3m8!1s0x46dbc515a1222995:0xc2af0b9d9d1229be!2sVsevprokat!8m2!3d53.8564378!4d27.6332316!9m1!1b1!16s%2Fg%2F11vdkcx2zy!3m7!1s0x46dbc515a1222995:0xc2af0b9d9d1229be!8m2!3d53.8564378!4d27.6332316!9m1!1b1!16s%2Fg%2F11vdkcx2zy?hl=ru-LT&entry=ttu&g_ep=EgoyMDI2MDcyOS4wIKXMDSoASAFQAw%3D%3D
- Yandex reviews: https://yandex.com/maps/org/vsevprokat_by/48335432707/reviews/?ll=27.520454%2C53.917639&z=17

## Source Files

Use this raw JSON link in the OpenCart module source settings:

- Минск, Кабушкина 94/2:
  `https://raw.githubusercontent.com/vsevprokatmsk-web/Google-Rewies/main/data/google-reviews-kabushkina-94-2.json`

## OpenCart Module Sources

Configure `Vsevprokat – Отзывы Google и Яндекс` with these sources:

1. Google
   - Ссылка на отзывы: Google reviews URL above
   - Ссылка на источник: raw JSON link above
   - Адрес локации: `Минск, Кабушкина 94/2`
   - Парсить от рейтинга: `4`

2. Яндекс
   - Ссылка на отзывы: Yandex reviews URL above
   - Ссылка на источник: leave empty
   - Адрес локации: `Минск, Кабушкина 94/2`
   - Парсить от рейтинга: `4`

## Manual Collection

Run locally:

```bash
npm install
npm run collect
```

Or start it from GitHub Actions with `Run workflow`.

## Schedule

The workflow runs every Monday at `00:00 UTC`, which is `03:00` in Minsk.

## Debug Data

Every run uploads a `google-browser-debug` artifact with:

- `data/status.json`;
- `data/google-reviews-kabushkina-94-2.json`;
- Google Maps HTML snapshots;
- visible text snapshots;
- screenshots.
