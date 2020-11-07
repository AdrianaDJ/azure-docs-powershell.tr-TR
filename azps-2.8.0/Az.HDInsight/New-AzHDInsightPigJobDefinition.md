---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: 3f40857c0388983a12217477db96cbbdbb94e815
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751824"
---
# <span data-ttu-id="8be47-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8be47-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="8be47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be47-102">SYNOPSIS</span></span>
<span data-ttu-id="8be47-103">Domuz iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8be47-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="8be47-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8be47-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be47-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8be47-105">DESCRIPTION</span></span>
<span data-ttu-id="8be47-106">**New-AzHDInsightPigJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir domuz Job nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8be47-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8be47-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8be47-107">EXAMPLES</span></span>

### <span data-ttu-id="8be47-108">Örnek 1: domuz iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8be47-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8be47-109">Bu komut bir domuz iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8be47-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="8be47-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8be47-110">PARAMETERS</span></span>

### <span data-ttu-id="8be47-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="8be47-111">-Arguments</span></span>
<span data-ttu-id="8be47-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be47-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="8be47-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="8be47-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="8be47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be47-114">-DefaultProfile</span></span>
<span data-ttu-id="8be47-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8be47-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8be47-116">-Dosya</span><span class="sxs-lookup"><span data-stu-id="8be47-116">-File</span></span>
<span data-ttu-id="8be47-117">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be47-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="8be47-118">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be47-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="8be47-119">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be47-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="8be47-120">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="8be47-120">-Files</span></span>
<span data-ttu-id="8be47-121">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be47-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="8be47-122">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="8be47-122">-Query</span></span>
<span data-ttu-id="8be47-123">Domuz sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be47-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="8be47-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="8be47-124">-StatusFolder</span></span>
<span data-ttu-id="8be47-125">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be47-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="8be47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be47-126">CommonParameters</span></span>
<span data-ttu-id="8be47-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8be47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be47-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be47-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be47-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8be47-129">INPUTS</span></span>

### <span data-ttu-id="8be47-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8be47-130">None</span></span>

## <span data-ttu-id="8be47-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8be47-131">OUTPUTS</span></span>

### <span data-ttu-id="8be47-132">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8be47-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="8be47-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8be47-133">NOTES</span></span>

## <span data-ttu-id="8be47-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8be47-134">RELATED LINKS</span></span>

[<span data-ttu-id="8be47-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8be47-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


