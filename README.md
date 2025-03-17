# Terraform Infrastructure as Code (IaC)

### Este repositório contém a infraestrutura como código (IaC) usando Terraform para gerenciar recursos em nuvem, com foco principal na AWS. Ele organiza a criação de diferentes recursos de forma modular e reutilizável.

A estrutura do projeto foi pensada para ser escalável e fácil de entender, permitindo que diferentes ambientes (como desenvolvimento, staging e produção) possam ser configurados separadamente.

```
terraform-project/
├── bucket-s3-simples/
│   ├── bucket.tf        # Definição do recurso S3
│   └── main.tf          # Arquivo principal de configuração do bucket S3
└── README.md            # Documentação do projeto
```

## Como Usar

### Pré-requisitos

- Ter o [Terraform](https://www.terraform.io/downloads.html) instalado.
- Ter uma conta na [AWS](https://aws.amazon.com/) com as permissões necessárias.

### Passos para Rodar

1. Clone este repositório:

   ```bash
   git clone https://github.com/Daviddevlinux/terraform-resources
   cd terraform-project #entre na pasta do recurso que será criado
   ```

Inicializar o Terraform: Inicialize o diretório para baixar os plugins e dependências necessários.

```bash
terraform init
```

Validar a Configuração: Antes de continuar, você pode validar o código Terraform.

```bash
terraform validate
```

Gerar o Plano com terraform plan: O comando terraform plan gera um plano de execução, mostrando exatamente o que o Terraform fará. Ele compara o estado atual da infraestrutura com a configuração definida no código Terraform, e exibe as mudanças que serão feitas.

```bash
terraform plan
```

Aplicar o Plano com terraform apply: Após revisar o plano gerado com o comando terraform plan, execute terraform apply para aplicar as alterações à sua infraestrutura.

```bash
terraform apply
```

Durante a execução do terraform apply, será solicitado que você confirme as ações. Digite yes para aplicar as mudanças.

---

Destruir os Recursos (se necessário): Se você quiser destruir os recursos criados, execute:

```bash
terraform destroy
```
