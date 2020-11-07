---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938488"
---
# <span data-ttu-id="96250-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="96250-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="96250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96250-102">SYNOPSIS</span></span>
<span data-ttu-id="96250-103">Bir kovan iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96250-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="96250-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96250-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96250-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96250-105">DESCRIPTION</span></span>
<span data-ttu-id="96250-106">**New-AzHDInsightHiveJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir Hive iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="96250-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="96250-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96250-107">EXAMPLES</span></span>

### <span data-ttu-id="96250-108">Örnek 1: yığın iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="96250-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="96250-109">Bu komut bir Hive iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96250-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="96250-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96250-110">PARAMETERS</span></span>

### <span data-ttu-id="96250-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="96250-111">-Arguments</span></span>
<span data-ttu-id="96250-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="96250-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="96250-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="96250-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="96250-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96250-114">-DefaultProfile</span></span>
<span data-ttu-id="96250-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="96250-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96250-116">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="96250-116">-Defines</span></span>
<span data-ttu-id="96250-117">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96250-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="96250-118">-Dosya</span><span class="sxs-lookup"><span data-stu-id="96250-118">-File</span></span>
<span data-ttu-id="96250-119">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="96250-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="96250-120">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="96250-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="96250-121">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="96250-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="96250-122">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="96250-122">-Files</span></span>
<span data-ttu-id="96250-123">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="96250-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="96250-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="96250-124">-JobName</span></span>
<span data-ttu-id="96250-125">İşin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96250-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="96250-126">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="96250-126">-Query</span></span>
<span data-ttu-id="96250-127">Kovan sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="96250-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="96250-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="96250-128">-RunAsFileJob</span></span>
<span data-ttu-id="96250-129">Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96250-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="96250-130">Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="96250-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="96250-131">Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="96250-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="96250-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="96250-132">-StatusFolder</span></span>
<span data-ttu-id="96250-133">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="96250-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="96250-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96250-134">CommonParameters</span></span>
<span data-ttu-id="96250-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96250-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96250-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96250-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96250-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96250-137">INPUTS</span></span>

### <span data-ttu-id="96250-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96250-138">None</span></span>

## <span data-ttu-id="96250-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96250-139">OUTPUTS</span></span>

### <span data-ttu-id="96250-140">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="96250-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="96250-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96250-141">NOTES</span></span>

## <span data-ttu-id="96250-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96250-142">RELATED LINKS</span></span>

[<span data-ttu-id="96250-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="96250-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


