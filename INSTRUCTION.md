kubectl get storageclass
kubectl describe pvc mypvc
First you need to get pod name.
kubectl get pods -n todoapp 
Run in browser http://localhost:30009
Or kubectl logs  todoapp-5bd84b74d7-6qvgk, where todoapp-5bd84b74d7-6qvgk is pod name.
If you see website or "[30/Jun/2026 14:51:01] "GET /api/health HTTP/1.1" 200 9" aplication is working.

How to validate: ConfigMap data is mounted as files in the right order and secret data is mounted as a file?
kubectl exec todoapp-5bd84b74d7-6qvgk -it -- sh
# ls
PYTHONUNBUFFERED
# cat PYTHONUNBUFFERED
1# cd ..
# ls
Dockerfile  accounts  api  configs  data  db.sqlite3  lists  manage.py  probes  requirements.txt  secrets  todolist
# cd secrets
# ls
SECRET_KEY
# cat SECRET_KEY       
@e2(yx)v&tgh3_s=0yja-i!dpebxsz^dg47x)-k&kq_3zf*9e*
# 
