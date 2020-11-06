---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 6f7045773dc1bf5582e2c480fd9e4aed283bf8ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590488"
---
# <span data-ttu-id="ad9f2-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ad9f2-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="ad9f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9f2-103">Bir Sqoop iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad9f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad9f2-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad9f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad9f2-105">DESCRIPTION</span></span>
<span data-ttu-id="ad9f2-106">**New-AzureRmHDInsightSqoopJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir Sqoop iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ad9f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad9f2-107">EXAMPLES</span></span>

### <span data-ttu-id="ad9f2-108">Örnek 1: bir Sqoop iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad9f2-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="ad9f2-109">Bu komut, bir Sqoop iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="ad9f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad9f2-110">PARAMETERS</span></span>

### <span data-ttu-id="ad9f2-111">-Komut</span><span class="sxs-lookup"><span data-stu-id="ad9f2-111">-Command</span></span>
<span data-ttu-id="ad9f2-112">Sqoop komutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="ad9f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9f2-113">-DefaultProfile</span></span>
<span data-ttu-id="ad9f2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ad9f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad9f2-115">-Dosya</span><span class="sxs-lookup"><span data-stu-id="ad9f2-115">-File</span></span>
<span data-ttu-id="ad9f2-116">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="ad9f2-117">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="ad9f2-118">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="ad9f2-119">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="ad9f2-119">-Files</span></span>
<span data-ttu-id="ad9f2-120">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="ad9f2-121">-Libya</span><span class="sxs-lookup"><span data-stu-id="ad9f2-121">-LibDir</span></span>
<span data-ttu-id="ad9f2-122">Sqoop işi için kitaplık dizinini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="ad9f2-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="ad9f2-123">-StatusFolder</span></span>
<span data-ttu-id="ad9f2-124">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="ad9f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9f2-125">CommonParameters</span></span>
<span data-ttu-id="ad9f2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9f2-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad9f2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9f2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad9f2-128">INPUTS</span></span>

### <span data-ttu-id="ad9f2-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ad9f2-129">None</span></span>
<span data-ttu-id="ad9f2-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ad9f2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad9f2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad9f2-131">OUTPUTS</span></span>

### <span data-ttu-id="ad9f2-132">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ad9f2-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="ad9f2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad9f2-133">NOTES</span></span>

## <span data-ttu-id="ad9f2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad9f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad9f2-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ad9f2-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


