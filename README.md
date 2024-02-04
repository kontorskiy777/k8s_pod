# k8s_pod
1. Создаем Pod из yaml
   
kubectl apply -f pod.yaml

2.Проверим результат, для чего выполним команду:

kubectl get pod - Через какое-то время Pod должен перейти в состояние Running

3. Скейлим приложение
   
nano pod.yaml
(-) name: my-pod
(+)  name: my-pod-1

4.Применяем изменения

kubectl apply -f pod.yaml

5. Проверяем результат
   
kubectl get pod
Результат = 2 pod с разными именами.
6.Посмотрим описание, для чего выполним команду:
kubectl describe pod my-pod
7. Чистим за собой кластер
kubectl delete pod --all

