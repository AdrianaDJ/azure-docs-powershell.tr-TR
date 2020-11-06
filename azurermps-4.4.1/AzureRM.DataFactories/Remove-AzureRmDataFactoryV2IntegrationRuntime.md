---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: bf29e12292fba12cc6a5b4f99cef1e13f9d9fd8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591774"
---
# <span data-ttu-id="4d460-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d460-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4d460-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d460-102">SYNOPSIS</span></span>
<span data-ttu-id="4d460-103">Tümleştirme çalışma zamanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d460-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d460-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d460-104">SYNTAX</span></span>

### <span data-ttu-id="4d460-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d460-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d460-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4d460-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d460-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="4d460-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d460-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d460-108">DESCRIPTION</span></span>
<span data-ttu-id="4d460-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i Integration Runtime 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d460-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="4d460-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d460-110">EXAMPLES</span></span>

### <span data-ttu-id="4d460-111">Örnek 1: Tümleştirme çalışma zamanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4d460-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="4d460-112">Bu komut, ' test-ayrılmış-IR ' adlı tümleştirme çalışma zamanını ' test-df ' adındaki Veri Fabrikası 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d460-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="4d460-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4d460-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="4d460-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d460-114">PARAMETERS</span></span>

### <span data-ttu-id="4d460-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4d460-115">-DataFactoryName</span></span>
<span data-ttu-id="4d460-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="4d460-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d460-117">-Force</span></span>
<span data-ttu-id="4d460-118">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="4d460-118">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d460-119">-InputObject</span></span>
<span data-ttu-id="4d460-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4d460-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d460-121">-Name</span></span>
<span data-ttu-id="4d460-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="4d460-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d460-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d460-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4d460-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4d460-125">-ResourceId</span></span>
<span data-ttu-id="4d460-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4d460-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d460-127">-Confirm</span></span>
<span data-ttu-id="4d460-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d460-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d460-129">-WhatIf</span></span>
<span data-ttu-id="4d460-130">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="4d460-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d460-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d460-131">-DefaultProfile</span></span>
<span data-ttu-id="4d460-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d460-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d460-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d460-133">CommonParameters</span></span>
<span data-ttu-id="4d460-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d460-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d460-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d460-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d460-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d460-136">INPUTS</span></span>

### <span data-ttu-id="4d460-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4d460-137">System.String</span></span>
<span data-ttu-id="4d460-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="4d460-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4d460-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d460-139">OUTPUTS</span></span>

### <span data-ttu-id="4d460-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="4d460-140">System.Object</span></span>

## <span data-ttu-id="4d460-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d460-141">NOTES</span></span>
<span data-ttu-id="4d460-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="4d460-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4d460-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d460-143">RELATED LINKS</span></span>

[<span data-ttu-id="4d460-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d460-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="4d460-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d460-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

