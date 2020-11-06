---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: 3e4748a8bc5e5c04868fb7c2d4179c07ea63c905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588208"
---
# <span data-ttu-id="b385d-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b385d-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="b385d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b385d-102">SYNOPSIS</span></span>
<span data-ttu-id="b385d-103">Bir kovan iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b385d-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b385d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b385d-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b385d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b385d-105">DESCRIPTION</span></span>
<span data-ttu-id="b385d-106">**New-AzureRmHDInsightHiveJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir Hive iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b385d-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b385d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b385d-107">EXAMPLES</span></span>

### <span data-ttu-id="b385d-108">Örnek 1: yığın iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b385d-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b385d-109">Bu komut bir Hive iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b385d-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="b385d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b385d-110">PARAMETERS</span></span>

### <span data-ttu-id="b385d-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="b385d-111">-Arguments</span></span>
<span data-ttu-id="b385d-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b385d-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b385d-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="b385d-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b385d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b385d-114">-DefaultProfile</span></span>
<span data-ttu-id="b385d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b385d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b385d-116">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="b385d-116">-Defines</span></span>
<span data-ttu-id="b385d-117">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b385d-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b385d-118">-Dosya</span><span class="sxs-lookup"><span data-stu-id="b385d-118">-File</span></span>
<span data-ttu-id="b385d-119">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b385d-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b385d-120">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b385d-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="b385d-121">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b385d-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b385d-122">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="b385d-122">-Files</span></span>
<span data-ttu-id="b385d-123">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b385d-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b385d-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="b385d-124">-JobName</span></span>
<span data-ttu-id="b385d-125">İşin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b385d-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="b385d-126">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="b385d-126">-Query</span></span>
<span data-ttu-id="b385d-127">Kovan sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b385d-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="b385d-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="b385d-128">-RunAsFileJob</span></span>
<span data-ttu-id="b385d-129">Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b385d-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="b385d-130">Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="b385d-130">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="b385d-131">Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="b385d-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="b385d-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b385d-132">-StatusFolder</span></span>
<span data-ttu-id="b385d-133">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b385d-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b385d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b385d-134">CommonParameters</span></span>
<span data-ttu-id="b385d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b385d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b385d-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b385d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b385d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b385d-137">INPUTS</span></span>

### <span data-ttu-id="b385d-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b385d-138">None</span></span>
<span data-ttu-id="b385d-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b385d-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b385d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b385d-140">OUTPUTS</span></span>

### <span data-ttu-id="b385d-141">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b385d-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="b385d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b385d-142">NOTES</span></span>

## <span data-ttu-id="b385d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b385d-143">RELATED LINKS</span></span>

[<span data-ttu-id="b385d-144">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b385d-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


