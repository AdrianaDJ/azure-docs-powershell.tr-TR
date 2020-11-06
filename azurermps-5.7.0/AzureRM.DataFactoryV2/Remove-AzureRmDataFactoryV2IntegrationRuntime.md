---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a2515b3713f449d25963af5952e233117e078ba9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586730"
---
# <span data-ttu-id="5fefe-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5fefe-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5fefe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fefe-102">SYNOPSIS</span></span>
<span data-ttu-id="5fefe-103">Tümleştirme çalışma zamanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5fefe-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fefe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fefe-104">SYNTAX</span></span>

### <span data-ttu-id="5fefe-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5fefe-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fefe-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="5fefe-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fefe-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="5fefe-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fefe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fefe-108">DESCRIPTION</span></span>
<span data-ttu-id="5fefe-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i Integration Runtime 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5fefe-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="5fefe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fefe-110">EXAMPLES</span></span>

### <span data-ttu-id="5fefe-111">Örnek 1: Tümleştirme çalışma zamanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5fefe-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="5fefe-112">Bu komut, ' test-ayrılmış-IR ' adlı tümleştirme çalışma zamanını ' test-df ' adındaki Veri Fabrikası 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5fefe-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="5fefe-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5fefe-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="5fefe-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fefe-114">PARAMETERS</span></span>

### <span data-ttu-id="5fefe-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5fefe-115">-DataFactoryName</span></span>
<span data-ttu-id="5fefe-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="5fefe-116">The data factory name.</span></span>

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

### <span data-ttu-id="5fefe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fefe-117">-DefaultProfile</span></span>
<span data-ttu-id="5fefe-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5fefe-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fefe-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5fefe-119">-Force</span></span>
<span data-ttu-id="5fefe-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="5fefe-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5fefe-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fefe-121">-InputObject</span></span>
<span data-ttu-id="5fefe-122">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5fefe-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="5fefe-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="5fefe-123">-Name</span></span>
<span data-ttu-id="5fefe-124">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="5fefe-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="5fefe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fefe-125">-ResourceGroupName</span></span>
<span data-ttu-id="5fefe-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5fefe-126">The resource group name.</span></span>

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

### <span data-ttu-id="5fefe-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5fefe-127">-ResourceId</span></span>
<span data-ttu-id="5fefe-128">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5fefe-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5fefe-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fefe-129">-Confirm</span></span>
<span data-ttu-id="5fefe-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fefe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fefe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fefe-131">-WhatIf</span></span>
<span data-ttu-id="5fefe-132">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="5fefe-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5fefe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fefe-133">CommonParameters</span></span>
<span data-ttu-id="5fefe-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fefe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fefe-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fefe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fefe-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fefe-136">INPUTS</span></span>

### <span data-ttu-id="5fefe-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5fefe-137">System.String</span></span>
<span data-ttu-id="5fefe-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="5fefe-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5fefe-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fefe-139">OUTPUTS</span></span>

### <span data-ttu-id="5fefe-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="5fefe-140">System.Object</span></span>

## <span data-ttu-id="5fefe-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fefe-141">NOTES</span></span>
<span data-ttu-id="5fefe-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="5fefe-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="5fefe-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fefe-143">RELATED LINKS</span></span>

[<span data-ttu-id="5fefe-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5fefe-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="5fefe-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5fefe-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

