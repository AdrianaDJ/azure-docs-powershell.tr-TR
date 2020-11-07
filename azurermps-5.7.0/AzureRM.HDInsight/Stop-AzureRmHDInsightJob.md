---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 82587d855b41a8112bac900f0efe6c4b30941eb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764716"
---
# <span data-ttu-id="06598-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06598-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="06598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06598-102">SYNOPSIS</span></span>
<span data-ttu-id="06598-103">Kümede belirtilen çalışan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="06598-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06598-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06598-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06598-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06598-105">DESCRIPTION</span></span>
<span data-ttu-id="06598-106">**Stop-AzureRmHDInsightJob** cmdlet 'i, bir Azure HDInsight kümesinde belirtilen çalışan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="06598-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="06598-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06598-107">EXAMPLES</span></span>

### <span data-ttu-id="06598-108">Örnek 1: belirtilen kümede bir işi durdurma</span><span class="sxs-lookup"><span data-stu-id="06598-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="06598-109">Bu komut,-Hadoop-001 adlı kümede bir işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="06598-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="06598-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06598-110">PARAMETERS</span></span>

### <span data-ttu-id="06598-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="06598-111">-ClusterName</span></span>
<span data-ttu-id="06598-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06598-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06598-113">-DefaultProfile</span></span>
<span data-ttu-id="06598-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="06598-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06598-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="06598-115">-HttpCredential</span></span>
<span data-ttu-id="06598-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06598-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06598-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="06598-117">-JobId</span></span>
<span data-ttu-id="06598-118">İşin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="06598-118">Specifies the job ID of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06598-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06598-119">-ResourceGroupName</span></span>
<span data-ttu-id="06598-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06598-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="06598-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06598-121">CommonParameters</span></span>
<span data-ttu-id="06598-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06598-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06598-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06598-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06598-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06598-124">INPUTS</span></span>

### <span data-ttu-id="06598-125">Dizisi</span><span class="sxs-lookup"><span data-stu-id="06598-125">String</span></span>
<span data-ttu-id="06598-126">' JobId ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="06598-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="06598-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06598-127">OUTPUTS</span></span>

### <span data-ttu-id="06598-128">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06598-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="06598-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06598-129">NOTES</span></span>

## <span data-ttu-id="06598-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06598-130">RELATED LINKS</span></span>

[<span data-ttu-id="06598-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06598-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="06598-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06598-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="06598-133">Bekle-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06598-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


