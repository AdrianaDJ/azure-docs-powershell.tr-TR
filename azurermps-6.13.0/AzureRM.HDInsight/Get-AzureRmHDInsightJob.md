---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: 1fb2ee80a6dafb005509265e6012380eebf5abd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590273"
---
# <span data-ttu-id="d571c-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d571c-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="d571c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d571c-102">SYNOPSIS</span></span>
<span data-ttu-id="d571c-103">Bir kümeden işlerin listesini alır ve bunları ters sırada listeler veya belirli bir iş alır.</span><span class="sxs-lookup"><span data-stu-id="d571c-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d571c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d571c-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d571c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d571c-105">DESCRIPTION</span></span>
<span data-ttu-id="d571c-106">**Get-AzureRmHDInsightJob** cmdlet 'i, belirli bir Azure HDInsight kümesinin en son işlerini, listenin en son işine sahip olacak şekilde ters sırada alır.</span><span class="sxs-lookup"><span data-stu-id="d571c-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="d571c-107">*JobId* parametresini sağlayarak belirli bir iş edinin.</span><span class="sxs-lookup"><span data-stu-id="d571c-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="d571c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d571c-108">EXAMPLES</span></span>

### <span data-ttu-id="d571c-109">Örnek 1: belirtilen Azure HDInsight kümesinin en son işlerini alma</span><span class="sxs-lookup"><span data-stu-id="d571c-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="d571c-110">Bu komut,-Hadoop-001 adlı kümenin tüm son işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d571c-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d571c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d571c-111">PARAMETERS</span></span>

### <span data-ttu-id="d571c-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d571c-112">-ClusterName</span></span>
<span data-ttu-id="d571c-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d571c-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d571c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d571c-114">-DefaultProfile</span></span>
<span data-ttu-id="d571c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d571c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d571c-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d571c-116">-HttpCredential</span></span>
<span data-ttu-id="d571c-117">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d571c-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d571c-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="d571c-118">-JobId</span></span>
<span data-ttu-id="d571c-119">Alınacak işin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d571c-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d571c-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="d571c-120">-NumOfJobs</span></span>
<span data-ttu-id="d571c-121">Alınacak iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d571c-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d571c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d571c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d571c-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d571c-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d571c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d571c-124">CommonParameters</span></span>
<span data-ttu-id="d571c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d571c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d571c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d571c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d571c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d571c-127">INPUTS</span></span>

### <span data-ttu-id="d571c-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d571c-128">None</span></span>

## <span data-ttu-id="d571c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d571c-129">OUTPUTS</span></span>

### <span data-ttu-id="d571c-130">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d571c-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d571c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d571c-131">NOTES</span></span>

## <span data-ttu-id="d571c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d571c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d571c-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d571c-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="d571c-134">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d571c-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="d571c-135">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d571c-135">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="d571c-136">Bekle-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d571c-136">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


