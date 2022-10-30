# Notas-Aula-Big-Data-AWS
Notas de aula dos serviços de Big Data da AWS
Descrição do Desafio

Vamos explorar o poder do SQL em uma ferramenta de BigData totalmente gerenciada na AWS, o Amazon Athena. Para isso, o expert apresenta na prática esse serviço de consultas interativas que facilita a análise de dados no Amazon S3 usando SQL padrão.

Neste desafio, você irá aprender ao mesmo tempo que desenvolve algo prático para o seu portfólio! Sendo assim, as seguintes tarefas serão realizadas:

Criar bucket no Amazon S3;
Criar Glue Crawler;
Criar aplicação no Amazon Athena;
Criar tabelas;
Eliminar recursos;
Visualizar dados no Amazon QuickSight.
Dica: você pode dar um "fork" no repositório para organizar melhor as suas alterações e evoluções, mantendo uma referência direta ao código original.

### Serviços utilizados nessa atividade prática
 - Amazon S3
 - Amazon Glue
 - Amazon Athena
 - Amazon QuickSight

### Etapas para desenvolvimento

### Criar bucket no Amazon S3

- Amazon S3 Console -> Buckets -> Create bucket -> Bucket name [nome_do bucket] - Create bucket
- Create folder (Criar uma pasta chamada ```/output``` e outra com o nome do seu conjunto de dados. Este nome irá definir o nome da tabela criada no Glue)
- Upload dos arquivos de dados localizados na pasta ```/data```

#### Criar Glue Crawler

- Amazon Glue Console -> Crawlers -> Add Crawler
- Source type [Data Stores] -> Crawl all folders
- Data store [S3] -> Include path [caminho do diretório dos dados de entrada]
- Create IAM Role
- Frequency [Run on demand]
- Database name [seu_nome_de_db]
- Group behavior [Create a single schema for each S3 path]
- Finish
- Databases -> Tables -> Visualizar dados das tabelas criadas

### Criar aplicação no Amazon Athena

- Query editor -> Settings -> Manage settings -> Query result location and encryption -> Browse S3 -> selecionar o bucket criado

- Selecionar Database -> criar queries (exemplos na pasta ```/src```)
- Verificar queries não salvas no bucket criado no S3
- Salavar queries -> Executar novamente -> Verificar no bucket criado no S3
