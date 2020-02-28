# forecast
2020_clean - исходные данные

Порядок ознакомления:

1) STLDecompose-nobfill (все шаги описал в комментариях)
2) STLDecompose-bfill (тоже самое, только 0 заменяются функцией bfill())
3) ARIMA-MS-MEAN (все шаги описал в комментариях + bfill())
4) ARIMA-MS-SUM (тоже самое, считаются не средние значения по месяцам, а сумма! + bfill())

5) Два других файла - это ARIMA без bfill(), числа почти не отличаются поэтому ими в принципе можно пренебречь.


Итого верными мне кажутся STLDecompose-bfill, ARIMA-MS-SUM, ARIMA-MS-nobfill-SUM, прогноз в разоне 14кк.


STLDecompose - https://github.com/jrmontag/STLDecompose/blob/master/STL-usage-example.ipynb
ARIMA - https://www.8host.com/blog/prognozirovanie-vremennyx-ryadov-s-pomoshhyu-arima-v-python-3/
