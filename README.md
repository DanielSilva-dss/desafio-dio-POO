# 📚 Bootcamp Manager - Projeto POO em Java  

**Desafio DIO**: Sistema de gerenciamento de Bootcamps com cursos, mentorias e devs.  

<p align="center">  
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"/>  
  <img src="https://img.shields.io/badge/OOP-FF5722?style=for-the-badge&logo=java&logoColor=white" alt="POO"/>  
</p>  

---

## 🎯 Objetivo  
Simular um sistema de Bootcamp onde:  
- **Devs** podem se inscrever em bootcamps.  
- **Cursos** e **Mentorias** são conteúdos com carga horária e XP.  
- Progresso é calculado conforme conteúdos concluídos.  

---

## ⚙️ Funcionalidades  
✔️ Cadastro de devs, cursos e mentorias.  
✔️ Inscrição em bootcamps.  
✔️ Cálculo de XP baseado em conteúdos concluídos.  
✔️ Relação de conteúdos inscritos/concluídos por dev.  

---

## 📦 Estrutura do Projeto  
```bash
src/  
├── br/com/dio/desafio/dominio/  
│   ├── Bootcamp.java       # Gerencia conteúdos e devs  
│   ├── Conteudo.java       # Classe abstrata (pai de Curso/Mentoria)  
│   ├── Curso.java          # Cursos com carga horária  
│   ├── Dev.java            # Participantes do bootcamp  
│   └── Mentoria.java       # Mentorias com data  
└── Main.java               # Exemplo de uso  
```

---

## 🛠️ Como Executar  
1. Clone o repositório:  
   ```bash
   git clone https://github.com/DanielSilva-dss/desafio-dio-POO.git
   ```
2. Compile e execute no terminal:  
   ```bash
   javac src/br/com/dio/desafio/dominio/*.java src/Main.java
   java -cp src Main
   ```

---

## 💡 Exemplo de Uso (Main.java)  
```java
// Cria cursos e mentorias  
Curso cursoJava = new Curso("Java Básico", 20);  
Mentoria mentoriaOO = new Mentoria("Orientação a Objetos", LocalDate.now());  

// Cria bootcamp e adiciona conteúdos  
Bootcamp bootcamp = new Bootcamp("Bootcamp Java Developer");  
bootcamp.getConteudos().add(cursoJava);  
bootcamp.getConteudos().add(mentoriaOO);  

// Inscreve dev  
Dev devDaniel = new Dev("Daniel");  
devDaniel.inscreverBootcamp(bootcamp);  
devDaniel.progredir();  // Conclui o primeiro conteúdo  

System.out.println("XP: " + devDaniel.calcularTotalXp());  // 20 XP  
```

---

## 📌 Conceitos de POO Aplicados  
- **Herança**: `Curso` e `Mentoria` herdam de `Conteudo`.  
- **Polimorfismo**: `calcularXp()` sobrescrito nas subclasses.  
- **Encapsulamento**: Atributos privados com getters/setters.  
- **Abstração**: Classe `Conteudo` abstrata.  

---

## 🔧 Melhorias Futuras (Roadmap)  
- [ ] Adicionar testes unitários (JUnit).  
- [ ] Persistência em banco de dados (JDBC ou Hibernate).  
- [ ] Validações de entrada (ex.: carga horária positiva).  
- [ ] Interface simples via console ou API REST.  

---

## 📄 Licença  
Este projeto está sob a licença MIT.  

---

<p align="center">  
  👨‍💻 Desenvolvido por <a href="https://github.com/DanielSilva-dss">Daniel Silva</a> para o desafio DIO.  
</p>  

--- 

### ✨ Dica para Entrevistas  
**Destaque:**  
- Como a estrutura do projeto segue boas práticas de POO.  
- Como você evoluiria o projeto (testes, banco de dados, etc.).  

--- 

🔗 **Link do Repositório**: [github.com/DanielSilva-dss/desafio-dio-POO](https://github.com/DanielSilva-dss/desafio-dio-POO)  

--- 

Esse README está formatado para GitHub e inclui:  
- **Visão geral** do projeto.  
- **Instruções claras** para execução.  
- **Destaque dos conceitos técnicos** (útil para entrevistas).  
- **Sugestões de evolução** (mostra proatividade).  

Se quiser, adicione um diagrama de classes (usando Mermaid ou imagem) para ilustrar melhor a estrutura! 🎨