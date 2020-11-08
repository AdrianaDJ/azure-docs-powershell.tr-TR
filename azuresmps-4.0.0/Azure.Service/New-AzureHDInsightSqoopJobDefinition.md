---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105915"
---
# <span data-ttu-id="eabc2-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eabc2-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="eabc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eabc2-102">SYNOPSIS</span></span>
<span data-ttu-id="eabc2-103">Yeni bir Sqoop işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="eabc2-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="eabc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eabc2-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eabc2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eabc2-105">DESCRIPTION</span></span>
<span data-ttu-id="eabc2-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="eabc2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="eabc2-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="eabc2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="eabc2-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="eabc2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="eabc2-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="eabc2-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="eabc2-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="eabc2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="eabc2-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="eabc2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="eabc2-112">**New-AzureHDInsightSqoopJobDefinition** cmdlet 'i, bir Azure HDInsight kümesinde çalışacak bir Sqoop işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eabc2-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="eabc2-113">Sqoop, Hadoop kümeleri ile ilişkisel veritabanları arasında veri aktarmak için bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="eabc2-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="eabc2-114">Bir SQL Server veritabanından bir Hadoop Dağıtılmış dosya sistemi 'ne (.) veri aktarmak için Sqoop 'yi kullanabilirsiniz, verileri Hadoop MapReduce ile dönüştürebilir ve ardından bu verileri SQL Server veritabanına geri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eabc2-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="eabc2-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eabc2-115">EXAMPLES</span></span>

### <span data-ttu-id="eabc2-116">Örnek 1: veri Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="eabc2-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="eabc2-117">Bu komut bir AzureSQL Server veritabanındaki bir tablodaki tüm satırları HDInsight kümesine aktaran bir Sqoop işi tanımlar ve ardından $SqoopJobDef değişkeninde iş tanımını depolar.</span><span class="sxs-lookup"><span data-stu-id="eabc2-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="eabc2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eabc2-118">PARAMETERS</span></span>

### <span data-ttu-id="eabc2-119">-Komut</span><span class="sxs-lookup"><span data-stu-id="eabc2-119">-Command</span></span>
<span data-ttu-id="eabc2-120">Bir Sqoop komutu ve bağımsız değişkenlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eabc2-120">Specifies a Sqoop command and its arguments.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabc2-121">-Dosya</span><span class="sxs-lookup"><span data-stu-id="eabc2-121">-File</span></span>
<span data-ttu-id="eabc2-122">Çalıştırılacak komutları içeren bir komut dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eabc2-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="eabc2-123">Komut dosyası.</span><span class="sxs-lookup"><span data-stu-id="eabc2-123">The script file must be located on WASB.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabc2-124">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="eabc2-124">-Files</span></span>
<span data-ttu-id="eabc2-125">Bir iş için gerekli olan. b dosyalarının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eabc2-125">Specifies the collection of WASB files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabc2-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="eabc2-126">-Profile</span></span>
<span data-ttu-id="eabc2-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eabc2-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eabc2-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="eabc2-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabc2-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="eabc2-129">-StatusFolder</span></span>
<span data-ttu-id="eabc2-130">Çıkış kodu ve görev günlükleri dahil olmak üzere, bir iş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eabc2-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabc2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabc2-131">CommonParameters</span></span>
<span data-ttu-id="eabc2-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eabc2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabc2-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eabc2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabc2-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eabc2-134">INPUTS</span></span>

## <span data-ttu-id="eabc2-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eabc2-135">OUTPUTS</span></span>

## <span data-ttu-id="eabc2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eabc2-136">NOTES</span></span>

## <span data-ttu-id="eabc2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eabc2-137">RELATED LINKS</span></span>

[<span data-ttu-id="eabc2-138">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eabc2-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="eabc2-139">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eabc2-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="eabc2-140">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eabc2-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="eabc2-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eabc2-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


