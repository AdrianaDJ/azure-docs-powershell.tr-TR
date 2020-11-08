---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105640"
---
# <span data-ttu-id="f51c3-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="f51c3-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="f51c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f51c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f51c3-103">İş için günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="f51c3-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="f51c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f51c3-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f51c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f51c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f51c3-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f51c3-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f51c3-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f51c3-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f51c3-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="f51c3-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f51c3-109">Küme oluştururken yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için, [Azure PowerShell kullanarak HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)'ta Linux tabanlı kümeler oluşturma konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="f51c3-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f51c3-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, [HDInsight 'de Hadoop Işlerini gönderme](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="f51c3-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f51c3-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [bkz.](https://msdn.microsoft.com/en-us/library/mt438705.aspx)</span><span class="sxs-lookup"><span data-stu-id="f51c3-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f51c3-112">**Get-AzureHDInsightJobOutput** cmdlet 'i, kümeyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="f51c3-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="f51c3-113">Standart çıktı, standart hata, görev günlükleri ve görev günlüklerinin bir özeti dahil olmak üzere çeşitli türde iş günlükleri alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f51c3-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="f51c3-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f51c3-114">EXAMPLES</span></span>

### <span data-ttu-id="f51c3-115">Örnek 1: iş çıktısını alın</span><span class="sxs-lookup"><span data-stu-id="f51c3-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="f51c3-116">İlk komut geçerli aboneliğin KIMLIĞINI alır ve $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f51c3-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="f51c3-117">İkinci komut $Clustername değişkeninde MyCluster adını depolar.</span><span class="sxs-lookup"><span data-stu-id="f51c3-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="f51c3-118">Üçüncü komut bir MapReduce iş tanımı oluşturur ve $WordCountJob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f51c3-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="f51c3-119">Komut, işi başlatmak için $WordCountJob işi **Start-AzureHDInsightJob** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="f51c3-120">Ayrıca, işlemin bitmesini beklemek için **wait-AzureHDInsightJob** cmdlet 'ine $WordCountJob geçirir ve ardından iş çıktısını almak için **Get-AzureHDInsightJobOutput** kullanır.</span><span class="sxs-lookup"><span data-stu-id="f51c3-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="f51c3-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f51c3-121">PARAMETERS</span></span>

### <span data-ttu-id="f51c3-122">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="f51c3-122">-Certificate</span></span>
<span data-ttu-id="f51c3-123">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-124">-Küme</span><span class="sxs-lookup"><span data-stu-id="f51c3-124">-Cluster</span></span>
<span data-ttu-id="f51c3-125">Bir küme belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-125">Specifies a cluster.</span></span>
<span data-ttu-id="f51c3-126">Bu cmdlet, bu parametrenin belirttiği kümeden iş günlüklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f51c3-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="f51c3-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="f51c3-128">Bu cmdlet 'in bir iş için görev günlüklerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

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

### <span data-ttu-id="f51c3-129">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="f51c3-129">-Endpoint</span></span>
<span data-ttu-id="f51c3-130">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="f51c3-131">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="f51c3-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="f51c3-132">-HostedService</span></span>
<span data-ttu-id="f51c3-133">Varsayılan ad boşluğunu kullanmak istemezseniz, bir HDInsight hizmeti ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="f51c3-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="f51c3-135">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="f51c3-136">-JobId</span></span>
<span data-ttu-id="f51c3-137">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="f51c3-138">-Profile</span></span>
<span data-ttu-id="f51c3-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f51c3-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f51c3-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f51c3-141">-Standara</span><span class="sxs-lookup"><span data-stu-id="f51c3-141">-StandardError</span></span>
<span data-ttu-id="f51c3-142">Bu cmdlet 'in bir işin StdErr çıkışını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

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

### <span data-ttu-id="f51c3-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="f51c3-143">-StandardOutput</span></span>
<span data-ttu-id="f51c3-144">Bu cmdlet 'in bir işin SdtOut çıktısını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

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

### <span data-ttu-id="f51c3-145">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="f51c3-145">-Subscription</span></span>
<span data-ttu-id="f51c3-146">Alınacak HDInsight kümesini içeren aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="f51c3-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="f51c3-148">Görev günlüklerinin depolanacağı yerel klasörü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51c3-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="f51c3-149">-TaskSummary</span></span>
<span data-ttu-id="f51c3-150">Bu cmdlet 'lerin görev günlüğü özetini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f51c3-150">Indicates that this cmdlets gets the task log summary.</span></span>

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

### <span data-ttu-id="f51c3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51c3-151">CommonParameters</span></span>
<span data-ttu-id="f51c3-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f51c3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51c3-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f51c3-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51c3-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f51c3-154">INPUTS</span></span>

## <span data-ttu-id="f51c3-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f51c3-155">OUTPUTS</span></span>

## <span data-ttu-id="f51c3-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f51c3-156">NOTES</span></span>

## <span data-ttu-id="f51c3-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f51c3-157">RELATED LINKS</span></span>

[<span data-ttu-id="f51c3-158">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f51c3-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="f51c3-159">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f51c3-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="f51c3-160">Bekle-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f51c3-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
