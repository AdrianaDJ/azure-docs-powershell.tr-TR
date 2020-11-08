---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106248"
---
# <span data-ttu-id="00116-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="00116-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="00116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00116-102">SYNOPSIS</span></span>
<span data-ttu-id="00116-103">Bir HDInsight kümesine kovan sorguları gönderir, sorgu yürütmenin ilerlemesini gösterir ve sorgu sonuçlarını tek bir işlemde alır.</span><span class="sxs-lookup"><span data-stu-id="00116-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="00116-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00116-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00116-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00116-105">DESCRIPTION</span></span>
<span data-ttu-id="00116-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="00116-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="00116-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="00116-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="00116-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="00116-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="00116-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="00116-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="00116-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="00116-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="00116-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00116-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="00116-112">**Invoke-AzureHDInsightHiveJob** cmdlet 'ı bir HDInsight kümesine kovan gönderir, sorgu yürütmenin ilerlemesini görüntüler ve sorgu sonuçlarını tek bir işlemde alır.</span><span class="sxs-lookup"><span data-stu-id="00116-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="00116-113">Sorgunun gönderileceği HDInsight kümesini belirtmek için **Invoke-AzureHDInsightHiveJob** ' i çalıştırmadan önce Use-AzureHDInsightCluster cmdlet 'ini çalıştırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="00116-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="00116-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00116-114">EXAMPLES</span></span>

### <span data-ttu-id="00116-115">Örnek 1: yığın sorgusu gönderme</span><span class="sxs-lookup"><span data-stu-id="00116-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="00116-116">İlk komut, geçerli abonelikteki bir kümeyi kovan sorgusunda kullanılmak üzere belirtmek için **Use-AzureHDInsightCluster** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="00116-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="00116-117">İkinci komut, Hive sorgusunu göndermek için **Invoke-AzureHDInsightHiveJob** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="00116-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="00116-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00116-118">PARAMETERS</span></span>

### <span data-ttu-id="00116-119">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="00116-119">-Arguments</span></span>
<span data-ttu-id="00116-120">Bir Hadoop işi için bağımsız değişken dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="00116-121">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="00116-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="00116-122">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="00116-122">-Defines</span></span>
<span data-ttu-id="00116-123">Bir iş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="00116-124">-Dosya</span><span class="sxs-lookup"><span data-stu-id="00116-124">-File</span></span>
<span data-ttu-id="00116-125">Bir Azure Blob depolama alanında, çalıştırılacak sorguyu içeren bir dosyanın Windows Azure depolama blob blob (. b) yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="00116-126">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00116-126">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="00116-127">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="00116-127">-Files</span></span>
<span data-ttu-id="00116-128">Bir kovan işi için gereken dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-128">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="00116-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="00116-129">-JobName</span></span>
<span data-ttu-id="00116-130">Bir kovan işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="00116-131">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan değeri kullanır: "kovan: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="00116-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="00116-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="00116-132">-Profile</span></span>
<span data-ttu-id="00116-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00116-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="00116-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00116-135">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="00116-135">-Query</span></span>
<span data-ttu-id="00116-136">Kovan sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-136">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="00116-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="00116-137">-RunAsFileJob</span></span>
<span data-ttu-id="00116-138">Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00116-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="00116-139">Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="00116-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="00116-140">Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="00116-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="00116-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="00116-141">-StatusFolder</span></span>
<span data-ttu-id="00116-142">Çıkış kodu ve görev günlükleri dahil olmak üzere, bir iş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00116-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="00116-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00116-143">CommonParameters</span></span>
<span data-ttu-id="00116-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00116-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00116-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00116-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00116-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00116-146">INPUTS</span></span>

## <span data-ttu-id="00116-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00116-147">OUTPUTS</span></span>

## <span data-ttu-id="00116-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00116-148">NOTES</span></span>

## <span data-ttu-id="00116-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00116-149">RELATED LINKS</span></span>

[<span data-ttu-id="00116-150">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00116-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="00116-151">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="00116-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


