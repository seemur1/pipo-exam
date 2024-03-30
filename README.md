__Домашнее Задание по "Промышленной Инженерии Программного Обеспечения"__

Сделал Кондаков Семен Васильевич, БПИ203.

За основу было взято приложение по подсчёту кол-ва заходов на сервер (https://docs.docker.com/compose/gettingstarted/)

## Сборка docker-образа

```shell
docker build -t pipo-exam/simple:latest .
docker push pipo-exam/simple:latest
```

## Конфигурируем кубер + подключаем его к заранее поднятому серверу

```shell
cp config ~/.kube/config
```

## Поднимаем на нём образы с локального устройства

```shell
kubectl apply -f simpleapp.yaml
kubectl apply -f simpledb.yaml
```

## Проверям на корректность работы

```shell
kubectl get pods
kubectl get services
```

## Результат:
<http://141.105.64.134:30390>
