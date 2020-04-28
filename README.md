# Airbnb estimate tracking

***DEMO: https://artyom-ivanov.github.io/airbnb-tracking/***

Тестовое использование клиентского API от airbnb, которое рассчитывает потенциальный доход от сдачи недвижимости через их сервис в зависимости от местоположения пользователя.

Из-за CORS-блокировки приходится в явном виде передавать координаты lat/long и использовать серверную прослойку https://cors-anywhere.herokuapp.com/.

### API
```
POST https://www.airbnb.ru/api/v2/earnings_estimate?key=KEY_FROM_CLIENT
```
body:
```(json)
{
  "page": "magic_doorway_wmpw",
  "currency": "RUB",
  "estimateParams": [
    {
      "guests": 4,
      "roomType": "PRIVATE",
      "duration": "WEEK"
    },
    {
      "guests": 4,
      "roomType": "PRIVATE",
      "duration": "MONTH"
    },
    {
      "guests": 4,
      "roomType": "PRIVATE",
      "duration": "YEAR"
    }
  ],
  "latlng": {
    "lat": LATITUDE,
    "lng": LONGITUDE
  }
}
```
