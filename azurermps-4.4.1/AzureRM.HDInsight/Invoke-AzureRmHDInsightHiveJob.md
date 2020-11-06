---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594692"
---
# <span data-ttu-id="d6643-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="d6643-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="d6643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6643-102">SYNOPSIS</span></span>
<span data-ttu-id="d6643-103">Bir HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.</span><span class="sxs-lookup"><span data-stu-id="d6643-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6643-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6643-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6643-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6643-105">DESCRIPTION</span></span>
<span data-ttu-id="d6643-106">**Invoke-AzureRmHDInsightHiveJob** cmdlet 'ı bir Azure HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.</span><span class="sxs-lookup"><span data-stu-id="d6643-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="d6643-107">Sorgu için kullanılacak kümeyi belirtmek üzere **Invoke-AzureRmHDInsightHiveJob** ' i çağırmadan önce Use-AzureRmHDInsightCluster cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6643-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="d6643-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6643-108">EXAMPLES</span></span>

### <span data-ttu-id="d6643-109">Örnek 1: bir Azure HDInsight kümesine yığın sorgusu gönderme</span><span class="sxs-lookup"><span data-stu-id="d6643-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="d6643-110">Bu komut, TABLOLARı-Hadoop-001 adlı kümeye gönderir.</span><span class="sxs-lookup"><span data-stu-id="d6643-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d6643-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6643-111">PARAMETERS</span></span>

### <span data-ttu-id="d6643-112">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d6643-112">-Arguments</span></span>
<span data-ttu-id="d6643-113">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="d6643-114">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="d6643-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d6643-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="d6643-115">-DefaultContainer</span></span>
<span data-ttu-id="d6643-116">Varsayılan Azure depolama hesabında HDInsight kümesinin kullandığı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="d6643-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d6643-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="d6643-118">HDInsight kümesinin kullandığı varsayılan depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-118">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="d6643-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d6643-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="d6643-120">HDInsight kümesinin kullandığı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-120">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="d6643-121">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="d6643-121">-Defines</span></span>
<span data-ttu-id="d6643-122">Bir iş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-122">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="d6643-123">-Dosya</span><span class="sxs-lookup"><span data-stu-id="d6643-123">-File</span></span>
<span data-ttu-id="d6643-124">Çalıştırılacak sorguyu içeren Azure depolama 'da bir dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-124">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="d6643-125">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6643-125">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="d6643-126">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="d6643-126">-Files</span></span>
<span data-ttu-id="d6643-127">Bir kovan işi için gereken dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-127">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="d6643-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="d6643-128">-JobName</span></span>
<span data-ttu-id="d6643-129">Bir kovan işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-129">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="d6643-130">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan değeri kullanır: "kovan: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="d6643-130">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="d6643-131">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="d6643-131">-Query</span></span>
<span data-ttu-id="d6643-132">Kovan sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-132">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="d6643-133">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="d6643-133">-RunAsFileJob</span></span>
<span data-ttu-id="d6643-134">Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6643-134">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="d6643-135">Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="d6643-135">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="d6643-136">Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="d6643-136">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="d6643-137">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d6643-137">-StatusFolder</span></span>
<span data-ttu-id="d6643-138">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6643-138">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="d6643-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6643-139">-DefaultProfile</span></span>
<span data-ttu-id="d6643-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6643-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6643-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6643-141">CommonParameters</span></span>
<span data-ttu-id="d6643-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6643-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6643-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6643-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6643-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6643-144">INPUTS</span></span>

## <span data-ttu-id="d6643-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6643-145">OUTPUTS</span></span>

### <span data-ttu-id="d6643-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d6643-146">System.String</span></span>

## <span data-ttu-id="d6643-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6643-147">NOTES</span></span>

## <span data-ttu-id="d6643-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6643-148">RELATED LINKS</span></span>

[<span data-ttu-id="d6643-149">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d6643-149">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


