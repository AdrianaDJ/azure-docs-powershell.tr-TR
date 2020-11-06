---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594749"
---
# <span data-ttu-id="59c05-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="59c05-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="59c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c05-102">SYNOPSIS</span></span>
<span data-ttu-id="59c05-103">Self-hosted Integration Runtime için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="59c05-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59c05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59c05-104">SYNTAX</span></span>

### <span data-ttu-id="59c05-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59c05-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="59c05-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="59c05-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="59c05-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="59c05-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="59c05-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59c05-108">DESCRIPTION</span></span>
<span data-ttu-id="59c05-109">Tümleştirme çalışma zamanı için anahtarları alma.</span><span class="sxs-lookup"><span data-stu-id="59c05-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="59c05-110">Anahtarlar, tümleştirme çalışma zamanı düğümünü kaydettirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="59c05-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="59c05-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59c05-111">EXAMPLES</span></span>

### <span data-ttu-id="59c05-112">Örnek 1: Tümleştirme çalışma zamanı anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="59c05-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="59c05-113">Cmdlet ' test-Selfhost-IR ' adlı bir tümleştirme çalışma zamanı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="59c05-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="59c05-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59c05-114">PARAMETERS</span></span>

### <span data-ttu-id="59c05-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="59c05-115">-DataFactoryName</span></span>
<span data-ttu-id="59c05-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="59c05-116">The data factory name.</span></span>

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

### <span data-ttu-id="59c05-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59c05-117">-InputObject</span></span>
<span data-ttu-id="59c05-118">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="59c05-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="59c05-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="59c05-119">-Name</span></span>
<span data-ttu-id="59c05-120">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="59c05-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="59c05-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c05-121">-ResourceGroupName</span></span>
<span data-ttu-id="59c05-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="59c05-122">The resource group name.</span></span>

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

### <span data-ttu-id="59c05-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="59c05-123">-ResourceId</span></span>
<span data-ttu-id="59c05-124">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="59c05-124">The Azure resource ID.</span></span>

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

## <span data-ttu-id="59c05-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59c05-125">INPUTS</span></span>

### <span data-ttu-id="59c05-126">System. String</span><span class="sxs-lookup"><span data-stu-id="59c05-126">System.String</span></span>
<span data-ttu-id="59c05-127">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="59c05-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="59c05-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59c05-128">OUTPUTS</span></span>

### <span data-ttu-id="59c05-129">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="59c05-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="59c05-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59c05-130">NOTES</span></span>

## <span data-ttu-id="59c05-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59c05-131">RELATED LINKS</span></span>
[<span data-ttu-id="59c05-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="59c05-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
