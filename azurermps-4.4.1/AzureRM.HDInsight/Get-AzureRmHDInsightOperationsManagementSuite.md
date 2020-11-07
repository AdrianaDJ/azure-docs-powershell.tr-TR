---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 0f3e9e542ff1d05a9872096a784c8dabfed1910b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764850"
---
# <span data-ttu-id="23daf-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="23daf-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="23daf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23daf-102">SYNOPSIS</span></span>
<span data-ttu-id="23daf-103">Kümedeki Operations Management Suite (OMS) yüklemesinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23daf-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23daf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23daf-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23daf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23daf-105">DESCRIPTION</span></span>
<span data-ttu-id="23daf-106">**Get-AzureRmHDInsightOperationsManagementSuite** cmdlet 'i, bir Azure HDıNSIGHT kümesindeki OMS yüklemesinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23daf-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="23daf-107">OMS etkinleştirilirse, ayrıca OMS çalışma alanı kimliği 'ni de döndürür.</span><span class="sxs-lookup"><span data-stu-id="23daf-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="23daf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23daf-108">EXAMPLES</span></span>

### <span data-ttu-id="23daf-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23daf-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="23daf-110">ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="23daf-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="23daf-111">Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği</span><span class="sxs-lookup"><span data-stu-id="23daf-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="23daf-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="23daf-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="23daf-113">ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="23daf-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="23daf-114">Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği</span><span class="sxs-lookup"><span data-stu-id="23daf-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="23daf-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="23daf-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="23daf-116">ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="23daf-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="23daf-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="23daf-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="23daf-118">ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="23daf-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="23daf-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23daf-119">PARAMETERS</span></span>

### <span data-ttu-id="23daf-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="23daf-120">-Name</span></span>
<span data-ttu-id="23daf-121">Işlem yönetim paketinin (OMS) durumunu almak için kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="23daf-121">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="23daf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23daf-122">-ResourceGroupName</span></span>
<span data-ttu-id="23daf-123">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="23daf-123">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="23daf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23daf-124">-DefaultProfile</span></span>
<span data-ttu-id="23daf-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23daf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23daf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23daf-126">CommonParameters</span></span>
<span data-ttu-id="23daf-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23daf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23daf-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23daf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23daf-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23daf-129">INPUTS</span></span>

### <span data-ttu-id="23daf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="23daf-130">System.String</span></span>

## <span data-ttu-id="23daf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23daf-131">OUTPUTS</span></span>

### <span data-ttu-id="23daf-132">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="23daf-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="23daf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23daf-133">NOTES</span></span>

## <span data-ttu-id="23daf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23daf-134">RELATED LINKS</span></span>

