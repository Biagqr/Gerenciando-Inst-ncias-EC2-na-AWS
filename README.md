O que é uma instância EC2

EC2 (Elastic Compute Cloud) é o serviço da AWS que permite criar servidores virtuais na nuvem.

Uma instância é simplesmente um servidor virtual rodando na AWS.

Você escolhe:

Tipo de instância → define CPU, memória e performance.

Sistema operacional → Linux, Windows, etc.

Storage → EBS (disco em nuvem) ou volumes adicionais.

2️⃣ Criando uma instância EC2

Passos básicos:

Escolher a AMI (Amazon Machine Image)

Pré-configuração do SO e software necessário.

Selecionar o tipo de instância

Ex.: t2.micro (gratuito no Free Tier), m5.large (mais potência).

Configurar rede e segurança

Sub-rede da VPC, grupo de segurança (firewall).

Adicionar storage

SSD ou HDD, tamanho do disco.

Configurar tags

Ex.: Nome da instância, ambiente (dev, prod).

Configurar Key Pair

Chave de acesso SSH (Linux) ou RDP (Windows).

Lançar a instância

3️⃣ Gerenciando instâncias EC2

Depois de criada, você pode gerenciar sua instância de várias formas:

🔹 Ações básicas

Start → Ligar a instância.

Stop → Desligar a instância (você não paga pelo tempo parado, mas paga pelo EBS).

Reboot → Reiniciar a instância.

Terminate → Apagar a instância permanentemente (cuidado, dados podem se perder se não tiver backup).

🔹 Monitoramento

Use CloudWatch para monitorar CPU, memória e tráfego de rede.

Configure Alarmes para notificar quando a instância estiver sobrecarregada.

🔹 Segurança

Security Groups → firewall da instância, permite ou bloqueia portas.

IAM Roles → define permissões de acesso a outros serviços AWS.

🔹 Backups

Snapshots do EBS → cria cópias do disco para recuperação.

AMIs personalizadas → cria imagem da instância para replicar em outros servidores.

4️⃣ Boas práticas

Escolher tipo correto de instância → evite pagar por mais do que precisa.

Habilitar Auto Scaling → aumenta/diminui instâncias automaticamente com demanda.

Manter snapshots regulares → evita perda de dados.

Usar tags e naming conventions → organiza o ambiente.

Aplicar patches e updates → manter segurança do SO.

Usuário → S3 → Lambda → EC2
        ↑               ↓
       Dados processados → S3 (opcional)

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/e6e0df57-10a7-4ac8-a478-eddbe0720426" />
