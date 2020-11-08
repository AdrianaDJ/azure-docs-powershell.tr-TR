---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105917"
---
# <span data-ttu-id="98277-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="98277-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="98277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98277-102">SYNOPSIS</span></span>
<span data-ttu-id="98277-103">HDInsight hizmeti için yeni bir kovan işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="98277-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="98277-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98277-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="98277-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98277-105">DESCRIPTION</span></span>
<span data-ttu-id="98277-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="98277-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="98277-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="98277-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="98277-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="98277-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="98277-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="98277-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="98277-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="98277-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="98277-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="98277-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="98277-112">**New-AzureHDInsightHiveJobDefinition** cmdlet 'ı bir Azure HDInsight hizmeti Için bir kovan işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="98277-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="98277-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98277-113">EXAMPLES</span></span>

### <span data-ttu-id="98277-114">Örnek 1: yığın iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="98277-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="98277-115">Bu komut, önceden tanımlanmış bir sorgu dizesi kullanan bir yığın iş tanımı oluşturur ve $HiveJobDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="98277-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="98277-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98277-116">PARAMETERS</span></span>

### <span data-ttu-id="98277-117">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="98277-117">-Arguments</span></span>
<span data-ttu-id="98277-118">Bir Hadoop işi için bağımsız değişken dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="98277-119">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="98277-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="98277-120">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="98277-120">-Defines</span></span>
<span data-ttu-id="98277-121">Bir iş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98277-122">-Dosya</span><span class="sxs-lookup"><span data-stu-id="98277-122">-File</span></span>
<span data-ttu-id="98277-123">Çalıştırılacak sorgu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="98277-124">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98277-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="98277-125">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="98277-125">-Files</span></span>
<span data-ttu-id="98277-126">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="98277-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="98277-127">-JobName</span></span>
<span data-ttu-id="98277-128">Tanımladığınız kovan işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="98277-129">Bu parametreyi belirtmezseniz, varsayılan ad kullanılır: "kovan: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="98277-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98277-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="98277-130">-Profile</span></span>
<span data-ttu-id="98277-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98277-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="98277-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98277-133">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="98277-133">-Query</span></span>
<span data-ttu-id="98277-134">Kovan sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-134">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98277-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="98277-135">-RunAsFileJob</span></span>
<span data-ttu-id="98277-136">Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98277-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="98277-137">Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="98277-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="98277-138">Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="98277-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98277-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="98277-139">-StatusFolder</span></span>
<span data-ttu-id="98277-140">Çıkış kodu ve görev günlükleri dahil olmak üzere, bir iş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98277-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="98277-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98277-141">CommonParameters</span></span>
<span data-ttu-id="98277-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98277-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98277-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98277-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98277-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98277-144">INPUTS</span></span>

## <span data-ttu-id="98277-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98277-145">OUTPUTS</span></span>

## <span data-ttu-id="98277-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98277-146">NOTES</span></span>

## <span data-ttu-id="98277-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98277-147">RELATED LINKS</span></span>

[<span data-ttu-id="98277-148">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="98277-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="98277-149">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="98277-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="98277-150">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="98277-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="98277-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="98277-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


