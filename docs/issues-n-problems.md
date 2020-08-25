#Project issues and problems.

##1. При формировании заказа возникает исключение ".. Delivery_address_id .. null".
    Возникает если в Order не заполнено поле Delivery address, т.к. оно пустое в профиле пользователя.
    Решения.
    1. Добавить поле Delivery address в профить пользователя и сделать его обязательным.
    2. В классе OrderController в метод createOrder() перед созданием заказа проверку на цельность заказа.
##2. При смене пароля возвращать на предыдущую страницу(reference).
##3. DataTime формат в БД не соответствует формату в thymeleaf.
    В thymeleaf: временная зона - Гринвич и другой формат.
    Временно поставил в admin/order-form.html на поле <input type="text" th:field="*{deliveryExpectedAt}">
    Решение.
    Попробовать применить loda-time.

    