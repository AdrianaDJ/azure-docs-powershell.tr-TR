---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: f51545cc28a11984c55fa05b6760b71a055de7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916599"
---
# <span data-ttu-id="87d2a-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="87d2a-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="87d2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="87d2a-103">Bir HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.</span><span class="sxs-lookup"><span data-stu-id="87d2a-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="87d2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87d2a-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87d2a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87d2a-105">DESCRIPTION</span></span>
<span data-ttu-id="87d2a-106">**Invoke-AzHDInsightHiveJob** cmdlet 'ı bir Azure HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.</span><span class="sxs-lookup"><span data-stu-id="87d2a-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="87d2a-107">Sorgu için kullanılacak kümeyi belirtmek üzere **Invoke-AzHDInsightHiveJob** ' i çağırmadan önce Use-AzHDInsightCluster cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="87d2a-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="87d2a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87d2a-108">EXAMPLES</span></span>

### <span data-ttu-id="87d2a-109">Örnek 1: bir Azure HDInsight kümesine yığın sorgusu gönderme</span><span class="sxs-lookup"><span data-stu-id="87d2a-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="87d2a-110">Bu komut, TABLOLARı-Hadoop-001 adlı kümeye gönderir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="87d2a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87d2a-111">PARAMETERS</span></span>

### <span data-ttu-id="87d2a-112">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="87d2a-112">-Arguments</span></span>
<span data-ttu-id="87d2a-113">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="87d2a-114">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-114">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="87d2a-115">-DefaultContainer</span></span>
<span data-ttu-id="87d2a-116">Varsayılan Azure depolama hesabında HDInsight kümesinin kullandığı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d2a-117">-DefaultProfile</span></span>
<span data-ttu-id="87d2a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="87d2a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="87d2a-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="87d2a-120">HDInsight kümesinin kullandığı varsayılan depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87d2a-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="87d2a-122">HDInsight kümesinin kullandığı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-123">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="87d2a-123">-Defines</span></span>
<span data-ttu-id="87d2a-124">Bir iş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-125">-Dosya</span><span class="sxs-lookup"><span data-stu-id="87d2a-125">-File</span></span>
<span data-ttu-id="87d2a-126">Çalıştırılacak sorguyu içeren Azure depolama 'da bir dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="87d2a-127">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87d2a-127">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-128">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="87d2a-128">-Files</span></span>
<span data-ttu-id="87d2a-129">Bir kovan işi için gereken dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-129">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="87d2a-130">-JobName</span></span>
<span data-ttu-id="87d2a-131">Bir kovan işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="87d2a-132">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan değeri kullanır: "kovan: \< ilk 100 karakter \> ".</span><span class="sxs-lookup"><span data-stu-id="87d2a-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-133">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="87d2a-133">-Query</span></span>
<span data-ttu-id="87d2a-134">Kovan sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-134">Specifies the Hive query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="87d2a-135">-RunAsFileJob</span></span>
<span data-ttu-id="87d2a-136">Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="87d2a-137">Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="87d2a-138">Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="87d2a-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="87d2a-139">-StatusFolder</span></span>
<span data-ttu-id="87d2a-140">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d2a-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d2a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d2a-141">CommonParameters</span></span>
<span data-ttu-id="87d2a-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87d2a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d2a-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d2a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d2a-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87d2a-144">INPUTS</span></span>

### <span data-ttu-id="87d2a-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="87d2a-145">None</span></span>

## <span data-ttu-id="87d2a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87d2a-146">OUTPUTS</span></span>

### <span data-ttu-id="87d2a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="87d2a-147">System.String</span></span>

## <span data-ttu-id="87d2a-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87d2a-148">NOTES</span></span>

## <span data-ttu-id="87d2a-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87d2a-149">RELATED LINKS</span></span>

[<span data-ttu-id="87d2a-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="87d2a-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)

