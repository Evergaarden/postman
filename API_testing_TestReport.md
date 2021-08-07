## Краткий отчет о прохождении тестов

Отчет будет представлен в формате:
+ Наименование задание и что нужно сделать
+ Тест для постмана
+ Скриншот результата 

1) Приходящий токен необходимо передать во все остальные запросы

        POST 162.55.220.72:5005/login
        Request
        login : str 
        password : str
    
`pm.environment.set("auth_token", pm.response.json().token);`
С помощью этого 



2) http://116.203.27.46:5002/user_info
req.
POST
age: int
salary: int
name: str
auth_token


resp.
{'start_qa_salary':salary,
 'qa_salary_after_6_months': salary * 2,
 'qa_salary_after_12_months': salary * 2.9,
 'person': {'u_name':[user_name, salary, age],
                                'u_age':age,
                                'u_salary_1.5_year': salary * 4}
                                }

Тесты:
1) Статус код 200
2) Проверка структуры json в ответе.
3) В ответе указаны коэффициенты умножения salary, напишите тесты по проверке правильности результата перемножения на коэффициент.
4) Достать значение из поля 'u_salary_1.5_year' и передать в поле salary запроса http://116.203.27.46:5002 (http://188.130.138.105:5001/new_data)/get_test_user
