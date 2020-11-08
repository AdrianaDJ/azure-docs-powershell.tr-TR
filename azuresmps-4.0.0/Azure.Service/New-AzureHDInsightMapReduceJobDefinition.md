---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105916"
---
# <span data-ttu-id="7d4a7-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7d4a7-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="7d4a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4a7-103">Yeni bir Maduce işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="7d4a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d4a7-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d4a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d4a7-105">DESCRIPTION</span></span>
<span data-ttu-id="7d4a7-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="7d4a7-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="7d4a7-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="7d4a7-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="7d4a7-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="7d4a7-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="7d4a7-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="7d4a7-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7d4a7-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="7d4a7-112">**New-AzureHDInsightMapReduceJobDefinition** cmdlet 'ı, Azure HDInsight kümesinde çalışacak yeni bir Maduce işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7d4a7-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d4a7-113">EXAMPLES</span></span>

### <span data-ttu-id="7d4a7-114">Örnek 1: MapReduce işi tanımlama, işi çalıştırma ve çıktıyı alma</span><span class="sxs-lookup"><span data-stu-id="7d4a7-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="7d4a7-115">İlk komut geçerli aboneliğin KIMLIĞINI alır ve $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="7d4a7-116">İkinci komut, MyCluster adını $Clustername değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="7d4a7-117">Üçüncü komut, MapReduce iş tanımı oluşturmak için **New-AzureHDInsightMapReduceJobDefinition** cmdlet 'ini kullanır ve ardından $WordCountJob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="7d4a7-118">Dördüncü komut şu cmdlet 'leri kullanarak bir dizi işlemi gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="7d4a7-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="7d4a7-119">**Start-AzureHDInsightJob** , $clustername işi başlatın.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="7d4a7-120">**Wait-AzureHDInsightJob-** işin bitmesini beklemek ve ilerlemenin ilerleme durumunu görüntülemek için bekleyin.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="7d4a7-121">İş çıktısını almak için **-AzureHDInsightJobOutput** .</span><span class="sxs-lookup"><span data-stu-id="7d4a7-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="7d4a7-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d4a7-122">PARAMETERS</span></span>

### <span data-ttu-id="7d4a7-123">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7d4a7-123">-Arguments</span></span>
<span data-ttu-id="7d4a7-124">Bir Hadoop işi için bağımsız değişken dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="7d4a7-125">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="7d4a7-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="7d4a7-126">-ClassName</span></span>
<span data-ttu-id="7d4a7-127">Java Arşivi (JAR) dosyasındaki iş sınıfının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4a7-128">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="7d4a7-128">-Defines</span></span>
<span data-ttu-id="7d4a7-129">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="7d4a7-130">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="7d4a7-130">-Files</span></span>
<span data-ttu-id="7d4a7-131">Bir iş için gerekli olan bir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="7d4a7-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="7d4a7-132">-JarFile</span></span>
<span data-ttu-id="7d4a7-133">MapReduce işinin kodunu ve bağımlılıklarını içeren bir JAR dosyasının tam nitelikli adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4a7-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="7d4a7-134">-JobName</span></span>
<span data-ttu-id="7d4a7-135">MapReduce işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="7d4a7-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-136">This parameter is optional.</span></span>
<span data-ttu-id="7d4a7-137">Bu parametreyi belirtmezseniz, *ClassName* parametresinin değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="7d4a7-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="7d4a7-138">-LibJars</span></span>
<span data-ttu-id="7d4a7-139">İşin LibJar başvuruları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="7d4a7-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="7d4a7-140">-Profile</span></span>
<span data-ttu-id="7d4a7-141">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d4a7-142">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d4a7-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="7d4a7-143">-StatusFolder</span></span>
<span data-ttu-id="7d4a7-144">Çıkış kodu ve görev günlükleri dahil olmak üzere, bir iş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="7d4a7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4a7-145">CommonParameters</span></span>
<span data-ttu-id="7d4a7-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d4a7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4a7-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4a7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4a7-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d4a7-148">INPUTS</span></span>

## <span data-ttu-id="7d4a7-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d4a7-149">OUTPUTS</span></span>

## <span data-ttu-id="7d4a7-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d4a7-150">NOTES</span></span>

## <span data-ttu-id="7d4a7-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d4a7-151">RELATED LINKS</span></span>

[<span data-ttu-id="7d4a7-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="7d4a7-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="7d4a7-153">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7d4a7-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="7d4a7-154">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7d4a7-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="7d4a7-155">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7d4a7-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="7d4a7-156">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7d4a7-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="7d4a7-157">Bekle-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7d4a7-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


