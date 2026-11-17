# Backup e Restore de Estações com Clonezilla

* **Aluno(a):** Iasminy Vitoria Caetano Rodrigues 
* **Tema:** Procedimento Técnico De Backup/Restore da UC 3.

## 1. Objetivo
Documenta o procedimento de backup e restore da UC3 usando Clonezila, para garantir que dá pra recuperar o sistema rapidamente se der falha e assim, manter todos os PCs padronizados. 

## 2. Ferramentas e Cuidados Técnicos
* ** Clonezilla live no arquivo .ISO, HD interno de tamanho igual ou superior.
* ** Usar pulseira anti-estatica, usar nobreak pra não desliga durante o procedimento, conferir espaço no HD interno antes e validar a imagem depois.

## 3. Passo a Passo
1. Ligar o PC Matriz pela imagem do Clonezila, escolher device-image e depois local_dev para escolher o HD interno.
2. Escolher savedisk para criar a imgem completa do disco e salvá-la em /home/partimag.
3. Exemplo:/home/partimag/backup-matriz-2026

## 4. Como Validar (Teste Final)
- Para confirmar que deu certo: PC ligou normal, sem tela azul ou erro de boot.
- Para confirmar que deu certo: Entrou no S.O. e arquivos de matriz aparecendo. 
