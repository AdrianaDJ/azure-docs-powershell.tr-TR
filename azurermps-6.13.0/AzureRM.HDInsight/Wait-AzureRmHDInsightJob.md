---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: de7df9417e617f88c61e75c64dd42f32b83fc66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590932"
---
# <span data-ttu-id="43034-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="43034-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="43034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43034-102">SYNOPSIS</span></span>
<span data-ttu-id="43034-103">Belirtilen işin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="43034-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43034-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43034-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43034-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43034-105">DESCRIPTION</span></span>
<span data-ttu-id="43034-106">**Wait-AzureRmHDInsightJob** cmdlet 'i, bir Azure HDInsight işinin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="43034-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="43034-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43034-107">EXAMPLES</span></span>

### <span data-ttu-id="43034-108">Örnek 1: işin tamamlanmasını veya başarısızlığını bekleme</span><span class="sxs-lookup"><span data-stu-id="43034-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="43034-109">Bu komut, bir işin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="43034-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="43034-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43034-110">PARAMETERS</span></span>

### <span data-ttu-id="43034-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="43034-111">-ClusterName</span></span>
<span data-ttu-id="43034-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43034-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="43034-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43034-113">-DefaultProfile</span></span>
<span data-ttu-id="43034-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="43034-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43034-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="43034-115">-HttpCredential</span></span>
<span data-ttu-id="43034-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43034-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="43034-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="43034-117">-JobId</span></span>
<span data-ttu-id="43034-118">İşin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="43034-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="43034-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43034-119">-ResourceGroupName</span></span>
<span data-ttu-id="43034-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43034-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="43034-121">-Timeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="43034-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="43034-122">Saniye cinsinden iş tamamlanması için beklenecek toplam süre.</span><span class="sxs-lookup"><span data-stu-id="43034-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="43034-123">-Waitıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="43034-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="43034-124">Saniye cinsinden iş durumu denetimleri arasında bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="43034-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="43034-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43034-125">CommonParameters</span></span>
<span data-ttu-id="43034-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43034-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43034-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43034-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43034-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43034-128">INPUTS</span></span>

### <span data-ttu-id="43034-129">System. String</span><span class="sxs-lookup"><span data-stu-id="43034-129">System.String</span></span>
<span data-ttu-id="43034-130">Parametreler: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43034-130">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="43034-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43034-131">OUTPUTS</span></span>

### <span data-ttu-id="43034-132">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="43034-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="43034-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43034-133">NOTES</span></span>

## <span data-ttu-id="43034-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43034-134">RELATED LINKS</span></span>

[<span data-ttu-id="43034-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="43034-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="43034-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="43034-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="43034-137">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="43034-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


