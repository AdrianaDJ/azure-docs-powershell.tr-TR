---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: b83e6604e854260814a949885d26968542e84efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588515"
---
# <span data-ttu-id="9cc24-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="9cc24-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="9cc24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc24-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc24-103">Self ile barındırılan tümleştirme çalışma zamanını yükseltir.</span><span class="sxs-lookup"><span data-stu-id="9cc24-103">Upgrades self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cc24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cc24-104">SYNTAX</span></span>

### <span data-ttu-id="9cc24-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cc24-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cc24-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9cc24-106">ByResourceId</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc24-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="9cc24-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc24-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cc24-108">DESCRIPTION</span></span>
<span data-ttu-id="9cc24-109">**Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet 'i, yeni sürüm kullanılabiliyorsa kendi içinde barındırılan tümleştirme çalışma zamanını yükseltir.</span><span class="sxs-lookup"><span data-stu-id="9cc24-109">The **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="9cc24-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cc24-110">EXAMPLES</span></span>

### <span data-ttu-id="9cc24-111">Örnek 1: kendini barındıran tümleştirme çalışma zamanını yükseltir</span><span class="sxs-lookup"><span data-stu-id="9cc24-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="9cc24-112">Cmdlet, ' test-Self-EU2 ' Veri Fabrikası içinde ' test-Selfhost-IR ' adlı Self olarak barındırılan tümleştirme çalışma zamanını yükseltir.</span><span class="sxs-lookup"><span data-stu-id="9cc24-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="9cc24-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cc24-113">PARAMETERS</span></span>

### <span data-ttu-id="9cc24-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9cc24-114">-DataFactoryName</span></span>
<span data-ttu-id="9cc24-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="9cc24-115">The data factory name.</span></span>

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

### <span data-ttu-id="9cc24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc24-116">-DefaultProfile</span></span>
<span data-ttu-id="9cc24-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cc24-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cc24-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cc24-118">-InputObject</span></span>
<span data-ttu-id="9cc24-119">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9cc24-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="9cc24-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cc24-120">-Name</span></span>
<span data-ttu-id="9cc24-121">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="9cc24-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="9cc24-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc24-122">-ResourceGroupName</span></span>
<span data-ttu-id="9cc24-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9cc24-123">The resource group name.</span></span>

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

### <span data-ttu-id="9cc24-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9cc24-124">-ResourceId</span></span>
<span data-ttu-id="9cc24-125">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="9cc24-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9cc24-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cc24-126">-Confirm</span></span>
<span data-ttu-id="9cc24-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cc24-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc24-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc24-128">-WhatIf</span></span>
<span data-ttu-id="9cc24-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cc24-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc24-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cc24-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc24-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc24-131">CommonParameters</span></span>
<span data-ttu-id="9cc24-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cc24-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc24-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cc24-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc24-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cc24-134">INPUTS</span></span>

### <span data-ttu-id="9cc24-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc24-135">System.String</span></span>

### <span data-ttu-id="9cc24-136">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="9cc24-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="9cc24-137">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9cc24-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9cc24-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cc24-138">OUTPUTS</span></span>

### <span data-ttu-id="9cc24-139">System. void</span><span class="sxs-lookup"><span data-stu-id="9cc24-139">System.Void</span></span>

## <span data-ttu-id="9cc24-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cc24-140">NOTES</span></span>
<span data-ttu-id="9cc24-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="9cc24-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="9cc24-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cc24-142">RELATED LINKS</span></span>

<span data-ttu-id="9cc24-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="9cc24-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

