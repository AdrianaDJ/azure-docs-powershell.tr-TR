---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: fd933d157748de424aa425179701897772d93569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594689"
---
# <span data-ttu-id="72fea-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="72fea-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="72fea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72fea-102">SYNOPSIS</span></span>
<span data-ttu-id="72fea-103">Bir kovan iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72fea-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72fea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72fea-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72fea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72fea-105">DESCRIPTION</span></span>
<span data-ttu-id="72fea-106">**New-AzureRmHDInsightHiveJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir Hive iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="72fea-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="72fea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72fea-107">EXAMPLES</span></span>

### <span data-ttu-id="72fea-108">Örnek 1: yığın iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="72fea-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="72fea-109">Bu komut bir Hive iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72fea-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="72fea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72fea-110">PARAMETERS</span></span>

### <span data-ttu-id="72fea-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="72fea-111">-Arguments</span></span>
<span data-ttu-id="72fea-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="72fea-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="72fea-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="72fea-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="72fea-114">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="72fea-114">-Defines</span></span>
<span data-ttu-id="72fea-115">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72fea-115">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="72fea-116">-Dosya</span><span class="sxs-lookup"><span data-stu-id="72fea-116">-File</span></span>
<span data-ttu-id="72fea-117">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72fea-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="72fea-118">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="72fea-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="72fea-119">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72fea-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="72fea-120">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="72fea-120">-Files</span></span>
<span data-ttu-id="72fea-121">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72fea-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="72fea-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="72fea-122">-JobName</span></span>
<span data-ttu-id="72fea-123">İşin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72fea-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="72fea-124">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="72fea-124">-Query</span></span>
<span data-ttu-id="72fea-125">Kovan sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72fea-125">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="72fea-126">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="72fea-126">-RunAsFileJob</span></span>
<span data-ttu-id="72fea-127">Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72fea-127">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="72fea-128">Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="72fea-128">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="72fea-129">Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="72fea-129">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="72fea-130">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="72fea-130">-StatusFolder</span></span>
<span data-ttu-id="72fea-131">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72fea-131">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="72fea-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fea-132">-DefaultProfile</span></span>
<span data-ttu-id="72fea-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72fea-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72fea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fea-134">CommonParameters</span></span>
<span data-ttu-id="72fea-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72fea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fea-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fea-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72fea-137">INPUTS</span></span>

## <span data-ttu-id="72fea-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72fea-138">OUTPUTS</span></span>

### <span data-ttu-id="72fea-139">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="72fea-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="72fea-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72fea-140">NOTES</span></span>

## <span data-ttu-id="72fea-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72fea-141">RELATED LINKS</span></span>

[<span data-ttu-id="72fea-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="72fea-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

