---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106009"
---
# <span data-ttu-id="159cf-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="159cf-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="159cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="159cf-102">SYNOPSIS</span></span>
<span data-ttu-id="159cf-103">Yeni bir akış MapReduce işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="159cf-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="159cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="159cf-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="159cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="159cf-105">DESCRIPTION</span></span>
<span data-ttu-id="159cf-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="159cf-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="159cf-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="159cf-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="159cf-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="159cf-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="159cf-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="159cf-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="159cf-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="159cf-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="159cf-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="159cf-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="159cf-112">**New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet 'ı bir Hadoop akış işinin parametrelerini temsil eden yeni bir iş tanımı nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="159cf-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="159cf-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="159cf-113">EXAMPLES</span></span>

### <span data-ttu-id="159cf-114">Örnek 1: bir akış MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="159cf-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="159cf-115">Bu komut belirtilen akış MapReduce iş tanımını oluşturur ve $StreamingWordCount değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="159cf-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="159cf-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="159cf-116">PARAMETERS</span></span>

### <span data-ttu-id="159cf-117">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="159cf-117">-Arguments</span></span>
<span data-ttu-id="159cf-118">Bir Hadoop işi için bağımsız değişken dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="159cf-119">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="159cf-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="159cf-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="159cf-120">-CmdEnv</span></span>
<span data-ttu-id="159cf-121">Bir iş veri düğümlerinde çalıştığında ayarlanacak komut satırı ortam değişkenleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

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

### <span data-ttu-id="159cf-122">-Combiner</span><span class="sxs-lookup"><span data-stu-id="159cf-122">-Combiner</span></span>
<span data-ttu-id="159cf-123">Bir Combiner dosya adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-123">Specifies a Combiner file name.</span></span>

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

### <span data-ttu-id="159cf-124">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="159cf-124">-Defines</span></span>
<span data-ttu-id="159cf-125">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="159cf-126">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="159cf-126">-Files</span></span>
<span data-ttu-id="159cf-127">Bir iş için gereken dosyalar dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-127">Specifies an array of files that are required for a job.</span></span>

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

### <span data-ttu-id="159cf-128">-Inputpath</span><span class="sxs-lookup"><span data-stu-id="159cf-128">-InputPath</span></span>
<span data-ttu-id="159cf-129">Giriş dosyalarının en fazla yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159cf-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="159cf-130">-JobName</span></span>
<span data-ttu-id="159cf-131">Yeni Maduce iş tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="159cf-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="159cf-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="159cf-133">-Mapper</span><span class="sxs-lookup"><span data-stu-id="159cf-133">-Mapper</span></span>
<span data-ttu-id="159cf-134">Eşleyici dosya adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-134">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="159cf-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="159cf-135">-OutputPath</span></span>
<span data-ttu-id="159cf-136">İş çıkışının en son yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159cf-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="159cf-137">-Profile</span></span>
<span data-ttu-id="159cf-138">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="159cf-139">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="159cf-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="159cf-140">-Reducer</span><span class="sxs-lookup"><span data-stu-id="159cf-140">-Reducer</span></span>
<span data-ttu-id="159cf-141">Bir Reducer dosya adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-141">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="159cf-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="159cf-142">-StatusFolder</span></span>
<span data-ttu-id="159cf-143">İş için, çıkış kodu ve görev günlükleri dahil standart çıktıları ve hata çıktılarını içeren klasörü belirtir.</span><span class="sxs-lookup"><span data-stu-id="159cf-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="159cf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159cf-144">CommonParameters</span></span>
<span data-ttu-id="159cf-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="159cf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159cf-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="159cf-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159cf-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="159cf-147">INPUTS</span></span>

## <span data-ttu-id="159cf-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="159cf-148">OUTPUTS</span></span>

## <span data-ttu-id="159cf-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="159cf-149">NOTES</span></span>

## <span data-ttu-id="159cf-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="159cf-150">RELATED LINKS</span></span>

[<span data-ttu-id="159cf-151">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="159cf-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="159cf-152">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="159cf-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="159cf-153">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="159cf-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="159cf-154">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="159cf-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


