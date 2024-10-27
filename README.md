# sre-devops_interviews
- [lunux/network](#lunuxnetwork)
- [k8s/docker](#k8sdocker)
- [databases](#databases)
- [ci/cd git](#cicd-git)
- [ansible/terraform](#ansibleterraform)
- [coding](#coding)
- [обшие вопросы по sre/devops](#обшие-вопросы-по-sredevops)

## Lunux/network
- TLS: рассказать как работает, обычно на примере HTTPS
- что такое copy on write?
- для чего помимо ping и traceroute используется ICMP
- что такое JWT
- NGINX: какие еще протоколы может обслуживать, помимо HTTP
- cfs scheduler или как выделяется процессорное время для процессов 
- что дают права +x на дирректорию?  
  - бит чтения отвечает за возможность выводить список файлов внутри директорий; бит записи — за возможность создания, изменения файлов внутри директории и изменения параметров директории; бит исполнения отвечает за возможность доступа к директории и файлам внутри директории.
- swap и java: в документации пишут для elasticsearch важно чтобы был выключен swap а для kafka без большой разницы, почему так?
- чем journalctl logs отличаются от обычных логов
- утилита locate, как работает и зачем нужна?
## k8s/docker
- перечисли типы docker networks и как каждая работает
- что такое NodePort 
  - 'https://kubernetes.io/docs/concepts/services-networking/service/#type-nodeport'
- Создадим под с label app=nginx и создадим деплоймент с таким же matchLabels и labels, возьмет ли депплоймент под управление этот под и как деплоймент понимает какие поды ему принадлежат?
- какие элемент cotrol plane имеют master election
- что такое drain и cordon, в чем их отличие?
- что такое multistage сборка?
- что такое CRI, CNI, CRD, CSI?
- как избежать нежелательного выселения подов в случае, если допустим другая команда решила повыселять ваши поды с общиз нод. 
  - PDB
- что такое Admission Controller
- что такое PVC?
## databases
- kafka: что надо сделать чтобы добавить консьюмера в консьюм группу ?
  - речь о добавлении партиций, несколько консьюмеров не могут читать из одной партиции
- типы хостов в elasticsearch и что каждый делает?
- CAP теорема и её расширение  PACELC
- ACID и BASE
- для какого типа данных нельзя создать индекс?
- Mysql: типы движков таблиц
## ci/cd git
- типы деплоев
- вот есть несколько репозиториев и тебе надо в каждый добавить одинаковую джобу
  - ожидается что расскажешь об git includes 
- чем rebase отличается от merge
## ansible/terraform
- чем отличается в ansible command от shell и от raw?
- terraform: чем отличается count от foreach
## coding
- что такое лямбда функции?
- что такое decorator в python
- какой элемент в python содержит не повторяющиеся элементы
  - set (множество по русски)
## обшие вопросы по sre/devops
- что такое metrics cardinality и чем это опасно?
- 4 золотых сигнала SRE
  - https://habr.com/ru/companies/flant/articles/462503/
- что такое SLI/SLO/SLA
- 12 factor app 
  - https://habr.com/ru/companies/slurm/articles/785658/
- Идеальный пайплайн 
  - https://habr.com/ru/companies/rabota/articles/560922/
- IAK какие подходы бывают, чем отличаются?
  - 'декларативный и императивный'
