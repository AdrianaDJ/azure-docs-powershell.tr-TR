---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594742"
---
# <span data-ttu-id="99714-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="99714-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="99714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99714-102">SYNOPSIS</span></span>
<span data-ttu-id="99714-103">Tümleştirme çalışma zamanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99714-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99714-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99714-104">SYNTAX</span></span>

### <span data-ttu-id="99714-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99714-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99714-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="99714-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99714-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="99714-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="99714-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="99714-108">DESCRIPTION</span></span>
<span data-ttu-id="99714-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i Integration Runtime 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99714-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="99714-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99714-110">EXAMPLES</span></span>

### <span data-ttu-id="99714-111">Örnek 1: Tümleştirme çalışma zamanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="99714-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="99714-112">Bu komut, ' test-ayrılmış-IR ' adlı tümleştirme çalışma zamanını ' test-df ' adındaki Veri Fabrikası 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99714-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="99714-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="99714-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="99714-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99714-114">PARAMETERS</span></span>

### <span data-ttu-id="99714-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="99714-115">-DataFactoryName</span></span>
<span data-ttu-id="99714-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="99714-116">The data factory name.</span></span>

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

### <span data-ttu-id="99714-117">-Force</span><span class="sxs-lookup"><span data-stu-id="99714-117">-Force</span></span>
<span data-ttu-id="99714-118">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="99714-118">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99714-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99714-119">-InputObject</span></span>
<span data-ttu-id="99714-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="99714-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="99714-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="99714-121">-Name</span></span>
<span data-ttu-id="99714-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="99714-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="99714-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99714-123">-ResourceGroupName</span></span>
<span data-ttu-id="99714-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="99714-124">The resource group name.</span></span>

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

### <span data-ttu-id="99714-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="99714-125">-ResourceId</span></span>
<span data-ttu-id="99714-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="99714-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="99714-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="99714-127">-Confirm</span></span>
<span data-ttu-id="99714-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99714-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99714-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99714-129">-WhatIf</span></span>
<span data-ttu-id="99714-130">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="99714-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="99714-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99714-131">INPUTS</span></span>

### <span data-ttu-id="99714-132">System. String</span><span class="sxs-lookup"><span data-stu-id="99714-132">System.String</span></span>
<span data-ttu-id="99714-133">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="99714-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="99714-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99714-134">OUTPUTS</span></span>

### <span data-ttu-id="99714-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="99714-135">System.Object</span></span>

## <span data-ttu-id="99714-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99714-136">NOTES</span></span>
<span data-ttu-id="99714-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="99714-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="99714-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99714-138">RELATED LINKS</span></span>
[<span data-ttu-id="99714-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="99714-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="99714-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="99714-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

