---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108092"
---
# <span data-ttu-id="ce178-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ce178-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="ce178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce178-102">SYNOPSIS</span></span>
<span data-ttu-id="ce178-103">Kümedeki yükleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ce178-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="ce178-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce178-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce178-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce178-105">DESCRIPTION</span></span>
<span data-ttu-id="ce178-106">**Get-AzHDInsightMonitoring** cmdlet 'i, bir Azure HDInsight kümesindeki izleme yüklemesinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ce178-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="ce178-107">İzleme etkinleştirilirse, Log Analytics çalışma alanı kimliği de döndürülür.</span><span class="sxs-lookup"><span data-stu-id="ce178-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="ce178-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce178-108">EXAMPLES</span></span>

### <span data-ttu-id="ce178-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ce178-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="ce178-110">ClusterMonitoringEnabled özelliği doğru olduğundan, kümede izleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ce178-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="ce178-111">Günlüklerin akışı olan izleme çalışma alanı kimliği 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="ce178-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="ce178-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ce178-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="ce178-113">ClusterMonitoringEnabled özelliği doğru olduğundan, kümede izleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ce178-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="ce178-114">Günlüklerin akışı olan izleme çalışma alanı kimliği 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="ce178-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="ce178-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ce178-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="ce178-116">ClusterMonitoringEnabled özelliği false olduğundan, kümede izleme devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ce178-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="ce178-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="ce178-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="ce178-118">ClusterMonitoringEnabled özelliği false olduğundan, kümede izleme devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ce178-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="ce178-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce178-119">PARAMETERS</span></span>

### <span data-ttu-id="ce178-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce178-120">-DefaultProfile</span></span>
<span data-ttu-id="ce178-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ce178-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce178-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce178-122">-Name</span></span>
<span data-ttu-id="ce178-123">İzleme durumunun alınacağı kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="ce178-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce178-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce178-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce178-125">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="ce178-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce178-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce178-126">CommonParameters</span></span>
<span data-ttu-id="ce178-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce178-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce178-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ce178-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce178-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce178-129">INPUTS</span></span>

### <span data-ttu-id="ce178-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ce178-130">System.String</span></span>

## <span data-ttu-id="ce178-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce178-131">OUTPUTS</span></span>

### <span data-ttu-id="ce178-132">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ce178-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="ce178-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce178-133">NOTES</span></span>

## <span data-ttu-id="ce178-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce178-134">RELATED LINKS</span></span>
