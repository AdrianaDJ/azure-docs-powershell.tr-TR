---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765194"
---
# <span data-ttu-id="1cf17-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="1cf17-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="1cf17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cf17-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf17-103">Tümleştirme çalışma zamanı için ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1cf17-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cf17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cf17-104">SYNTAX</span></span>

### <span data-ttu-id="1cf17-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1cf17-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="1cf17-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="1cf17-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="1cf17-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="1cf17-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="1cf17-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cf17-108">DESCRIPTION</span></span>
<span data-ttu-id="1cf17-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet 'i, veri fabrikasında Integration Runtime hakkında ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1cf17-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="1cf17-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cf17-110">EXAMPLES</span></span>

### <span data-ttu-id="1cf17-111">Örnek 1: Tümleştirme çalışma zamanı ölçüsünü alma</span><span class="sxs-lookup"><span data-stu-id="1cf17-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="1cf17-112">Bu komut, ' RG-test-dfv2 ' ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında ölçüm verilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="1cf17-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="1cf17-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cf17-113">PARAMETERS</span></span>

### <span data-ttu-id="1cf17-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1cf17-114">-DataFactoryName</span></span>
<span data-ttu-id="1cf17-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="1cf17-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cf17-116">-InputObject</span></span>
<span data-ttu-id="1cf17-117">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1cf17-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1cf17-118">-Name</span></span>
<span data-ttu-id="1cf17-119">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="1cf17-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf17-120">-ResourceGroupName</span></span>
<span data-ttu-id="1cf17-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1cf17-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1cf17-122">-ResourceId</span></span>
<span data-ttu-id="1cf17-123">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="1cf17-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="1cf17-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cf17-124">INPUTS</span></span>

### <span data-ttu-id="1cf17-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1cf17-125">System.String</span></span>
<span data-ttu-id="1cf17-126">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="1cf17-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="1cf17-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cf17-127">OUTPUTS</span></span>

### <span data-ttu-id="1cf17-128">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimeölçüler</span><span class="sxs-lookup"><span data-stu-id="1cf17-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="1cf17-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cf17-129">NOTES</span></span>

## <span data-ttu-id="1cf17-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cf17-130">RELATED LINKS</span></span>
[<span data-ttu-id="1cf17-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1cf17-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

