\#DevOps Lab 4 — Ansible basics (nginx + index.html)



\## Что сделано

Ansible-плейбук устанавливает nginx на VM2 и копирует страницу `index.html` в `/var/www/html/index.html`.



\## Стенд

\- VM1 (Control): 10.0.2.15 (SSH: `ssh student@127.0.0.1 -p 2222`)

\- VM2 (Managed): 10.0.2.16 (SSH: `ssh student@127.0.0.1 -p 2223`)

\- NAT Network: 10.0.2.0/24

\- Проверка из Windows: http://127.0.0.1:8080 (проброс 8080 -> VM2:80)



\## Структура репозитория

\- `src/` — playbook и файлы Ansible

\- `screenshots/` — скриншоты выполнения

\- `check\_diff.log` — запуск `--check --diff`

\- `run.log` — запуск плейбука

\- `curl\_vm2.log` — проверка `curl`



\## Запуск (на VM1)

```bash

cd ~/DevOpsLab4/src

ansible-playbook playbook.yml --check --diff

ansible-playbook playbook.yml



