---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106010"
---
# <span data-ttu-id="32dea-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="32dea-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="32dea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32dea-102">SYNOPSIS</span></span>
<span data-ttu-id="32dea-103">HDInsight hizmeti için yeni bir domuz işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="32dea-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="32dea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32dea-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="32dea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="32dea-105">DESCRIPTION</span></span>
<span data-ttu-id="32dea-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="32dea-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="32dea-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="32dea-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="32dea-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="32dea-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="32dea-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="32dea-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="32dea-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="32dea-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="32dea-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32dea-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="32dea-112">**New-AzureHDInsightPigJobDefinition** , bir Azure HDInsight hizmeti Için bir domuz işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="32dea-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="32dea-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32dea-113">EXAMPLES</span></span>

### <span data-ttu-id="32dea-114">Örnek 1: yeni bir domuz işi tanımlama</span><span class="sxs-lookup"><span data-stu-id="32dea-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="32dea-115">İlk komut bir dize değeri bildirir ve $0 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="32dea-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="32dea-116">İkinci komut domuz iş sorgusu oluşturur ve $QueryString değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="32dea-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="32dea-117">Son komutu $QueryString sorguyu kullanan bir domuz iş tanımı oluşturur ve iş tanımını $PigJobDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="32dea-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="32dea-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32dea-118">PARAMETERS</span></span>

### <span data-ttu-id="32dea-119">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="32dea-119">-Arguments</span></span>
<span data-ttu-id="32dea-120">Bir domuz işi için bağımsız değişken dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dea-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="32dea-121">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="32dea-121">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32dea-122">-Dosya</span><span class="sxs-lookup"><span data-stu-id="32dea-122">-File</span></span>
<span data-ttu-id="32dea-123">Çalıştırılacak sorgu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dea-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="32dea-124">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="32dea-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="32dea-125">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="32dea-125">-Files</span></span>
<span data-ttu-id="32dea-126">Bir domuz işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dea-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="32dea-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="32dea-127">-Profile</span></span>
<span data-ttu-id="32dea-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dea-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32dea-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="32dea-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32dea-130">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="32dea-130">-Query</span></span>
<span data-ttu-id="32dea-131">Domuz iş sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dea-131">Specifies a Pig job query.</span></span>

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

### <span data-ttu-id="32dea-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="32dea-132">-StatusFolder</span></span>
<span data-ttu-id="32dea-133">Çıkış kodu ve görev günlükleri dahil olmak üzere, bir iş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dea-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="32dea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32dea-134">CommonParameters</span></span>
<span data-ttu-id="32dea-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32dea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32dea-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32dea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32dea-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32dea-137">INPUTS</span></span>

## <span data-ttu-id="32dea-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32dea-138">OUTPUTS</span></span>

## <span data-ttu-id="32dea-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32dea-139">NOTES</span></span>

## <span data-ttu-id="32dea-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32dea-140">RELATED LINKS</span></span>

[<span data-ttu-id="32dea-141">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="32dea-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="32dea-142">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="32dea-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="32dea-143">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="32dea-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="32dea-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="32dea-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


