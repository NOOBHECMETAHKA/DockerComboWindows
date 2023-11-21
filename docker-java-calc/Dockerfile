# Образ в котором будет собираться калькулятор
FROM ubuntu
# Установка пакето для работы с jdk файлами и графическим интерфейсом
RUN apt-get update && apt-get install -y \
x11-apps \
xauth \
openjdk-11-jre \
&& rm -rf /var/lib/apt/lists/*
# Перенос приложения калькулятор в отдельный каталог для приложений
COPY calc.jar /new-app/
# Установка стандартного приложения
ENV DISPLAY=:0
# Запуск скомпилированного кода с помощью команды java -jar calc.jar
CMD [ "java", "-jar", "/new-app/calc.jar" ]


