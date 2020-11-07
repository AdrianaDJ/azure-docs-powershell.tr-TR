---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916632"
---
# <span data-ttu-id="7e9f5-101">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="7e9f5-101">Get-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="7e9f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9f5-103">Kümedeki Operations Management Suite (OMS) yüklemesinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

## <span data-ttu-id="7e9f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e9f5-104">SYNTAX</span></span>

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e9f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e9f5-105">DESCRIPTION</span></span>
<span data-ttu-id="7e9f5-106">**Get-AzHDInsightOperationsManagementSuite** cmdlet 'i, bir Azure HDıNSIGHT kümesindeki OMS yüklemesinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-106">The **Get-AzHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="7e9f5-107">OMS etkinleştirilirse, ayrıca OMS çalışma alanı kimliği 'ni de döndürür.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="7e9f5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e9f5-108">EXAMPLES</span></span>

### <span data-ttu-id="7e9f5-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e9f5-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="7e9f5-110">ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="7e9f5-111">Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği</span><span class="sxs-lookup"><span data-stu-id="7e9f5-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="7e9f5-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e9f5-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="7e9f5-113">ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="7e9f5-114">Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği</span><span class="sxs-lookup"><span data-stu-id="7e9f5-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="7e9f5-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7e9f5-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="7e9f5-116">ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="7e9f5-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="7e9f5-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="7e9f5-118">ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="7e9f5-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e9f5-119">PARAMETERS</span></span>

### <span data-ttu-id="7e9f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e9f5-120">-DefaultProfile</span></span>
<span data-ttu-id="7e9f5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7e9f5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e9f5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e9f5-122">-Name</span></span>
<span data-ttu-id="7e9f5-123">Işlem yönetim paketinin (OMS) durumunu almak için kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e9f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e9f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e9f5-125">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="7e9f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9f5-126">CommonParameters</span></span>
<span data-ttu-id="7e9f5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9f5-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9f5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9f5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e9f5-129">INPUTS</span></span>

### <span data-ttu-id="7e9f5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7e9f5-130">System.String</span></span>

## <span data-ttu-id="7e9f5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e9f5-131">OUTPUTS</span></span>

### <span data-ttu-id="7e9f5-132">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7e9f5-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="7e9f5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e9f5-133">NOTES</span></span>

## <span data-ttu-id="7e9f5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e9f5-134">RELATED LINKS</span></span>
