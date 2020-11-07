---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: f2c162427abc1a05c7680e0fc19e0d2406c3e4a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916547"
---
# <span data-ttu-id="4a298-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4a298-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="4a298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a298-102">SYNOPSIS</span></span>
<span data-ttu-id="4a298-103">Kümede belirtilen çalışan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="4a298-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="4a298-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a298-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a298-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a298-105">DESCRIPTION</span></span>
<span data-ttu-id="4a298-106">**Stop-AzHDInsightJob** cmdlet 'i, bir Azure HDInsight kümesinde belirtilen çalışan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="4a298-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4a298-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a298-107">EXAMPLES</span></span>

### <span data-ttu-id="4a298-108">Örnek 1: belirtilen kümede bir işi durdurma</span><span class="sxs-lookup"><span data-stu-id="4a298-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="4a298-109">Bu komut,-Hadoop-001 adlı kümede bir işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="4a298-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4a298-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a298-110">PARAMETERS</span></span>

### <span data-ttu-id="4a298-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4a298-111">-ClusterName</span></span>
<span data-ttu-id="4a298-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a298-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4a298-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a298-113">-DefaultProfile</span></span>
<span data-ttu-id="4a298-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4a298-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a298-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4a298-115">-HttpCredential</span></span>
<span data-ttu-id="4a298-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a298-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a298-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="4a298-117">-JobId</span></span>
<span data-ttu-id="4a298-118">İşin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a298-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a298-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a298-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a298-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a298-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4a298-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a298-121">CommonParameters</span></span>
<span data-ttu-id="4a298-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a298-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a298-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a298-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a298-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a298-124">INPUTS</span></span>

### <span data-ttu-id="4a298-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4a298-125">System.String</span></span>

## <span data-ttu-id="4a298-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a298-126">OUTPUTS</span></span>

### <span data-ttu-id="4a298-127">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4a298-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="4a298-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a298-128">NOTES</span></span>

## <span data-ttu-id="4a298-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a298-129">RELATED LINKS</span></span>

[<span data-ttu-id="4a298-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4a298-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="4a298-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4a298-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="4a298-132">Bekle-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4a298-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


