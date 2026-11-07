
# MER - Sorriso Metálico

### Entidades e atributos

#### 👤 PACIENTE

* id_paciente (PK)
* nome
* cpf
* vip

#### 🦷 DENTISTA

* id_dentista (PK)
* nome

#### 📅 CONSULTA

* id_consulta (PK)
* data
* horario
* status
* procedimento
* anotacao
* id_paciente (FK)
* id_dentista (FK)

### Relacionamentos

* 1 PACIENTE tem N CONSULTAS (1:N)
* 1 DENTISTA atende N CONSULTAS (1:N)

### RN's

* Um dentista não pode ter duas consultas na mesma data e horário (REQ04)
* Sábado, das 8h às 12h, do Dr. Roberto: somente pacientes com vip = verdadeiro (REQ06)
* Pacientes VIP têm prioridade nos horários da semana (REQ07)
* A recepção não vê a anotacao; o Dr. Roberto (CEO) vê tudo (REQ09 e REQ10)

### DER

![Diagrama DER](./database/der.png)

