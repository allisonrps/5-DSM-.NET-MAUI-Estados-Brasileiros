# 🚀 **Estados Brasileiros - .NET MAUI + MySQL (Azure VM)**

Aplicativo Android para cadastro e listagem de estados brasileiros, utilizando **.NET MAUI** e armazenando dados em um **banco MySQL hospedado em uma VM Azure**.

---

## 📌 **Funcionalidades**
✔ Cadastro de estados (Nome, Sigla, URL da bandeira)  
✔ Listagem dinâmica dos estados  
✔ Armazenamento em MySQL na nuvem (Azure VM)  
✔ Validação básica de formulário  

---

## 🛠 **Tecnologias**
- C# .NET MAUI 8.0+
- Android
- MySQL 8.0
- Azure Virtual Machine (Ubuntu Server)

---

## 🖼 **Telas do Aplicativo**

| Splash | Banco OFF | Banco ON | Lista Estados |
|-----------|-----------|-----------|-----------|
| ![SPLASH](/Prints/splash.png)| ![OFF](/Prints/tela_dboff.png) | ![ON](/Prints/tela_dbon.png) | ![Lista](/Prints/tela_estados.png) |

| MySQL Workbench | VM Azure |
|-----------------|----------|
| ![MySQL](/Prints/mysql_workbench.png) | ![Azure](/Prints/vm_azure.png) |

---
**VIDEO DEMONSTRATIVO**

[▶️ CLIQUE AQUI PARA BAIXAR](Prints/VideoDemo.mp4)

---

## ⚙ **Configuração**

### Pré-requisitos
- Visual Studio 2022 (com workload MAUI)
- Máquina Virtual Azure com:
  - MySQL Server instalado
  - Porta 3306 liberada
  - Usuário/Senha configurados

### Banco de Dados
```sql
CREATE DATABASE Estados;

USE Estados;

CREATE TABLE Estados (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    sigla CHAR(2) NOT NULL,
    url_bandeira VARCHAR(255),
);