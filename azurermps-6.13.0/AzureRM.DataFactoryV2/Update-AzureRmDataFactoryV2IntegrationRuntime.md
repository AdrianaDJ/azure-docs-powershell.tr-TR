---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 2c20752dd1e29962f128f687344b3b165f0a09ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590316"
---
# <span data-ttu-id="8a0a4-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8a0a4-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="8a0a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0a4-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a0a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a0a4-104">SYNTAX</span></span>

### <span data-ttu-id="8a0a4-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a0a4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0a4-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8a0a4-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0a4-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="8a0a4-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a0a4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a0a4-108">DESCRIPTION</span></span>
<span data-ttu-id="8a0a4-109">**Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet 'i Integration Runtime özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="8a0a4-110">Şu anda cmdlet, self-hosted Integration Runtime için yalnızca ' otomatik güncelleştirme ' ve ' AutoUpdateDelayOffset ' güncelleştirmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="8a0a4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a0a4-111">EXAMPLES</span></span>

### <span data-ttu-id="8a0a4-112">Örnek 1: Tümleştirme çalışma zamanını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="8a0a4-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="8a0a4-113">Cmdlet, ' test-Selfhost-IR ' adlı Self olarak barındırılan tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="8a0a4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a0a4-114">PARAMETERS</span></span>

### <span data-ttu-id="8a0a4-115">-Otomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8a0a4-115">-AutoUpdate</span></span>
<span data-ttu-id="8a0a4-116">Self-hosted Integration Runtime otomatik güncelleştirmesini etkinleştirin veya devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0a4-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="8a0a4-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="8a0a4-118">Self-hosted Integration Runtime otomatik güncelleştirmesi için günün saat olarak saat başı.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0a4-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8a0a4-119">-DataFactoryName</span></span>
<span data-ttu-id="8a0a4-120">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-120">The data factory name.</span></span>

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

### <span data-ttu-id="8a0a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0a4-121">-DefaultProfile</span></span>
<span data-ttu-id="8a0a4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a0a4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a0a4-123">-InputObject</span></span>
<span data-ttu-id="8a0a4-124">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="8a0a4-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a0a4-125">-Name</span></span>
<span data-ttu-id="8a0a4-126">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="8a0a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a0a4-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-128">The resource group name.</span></span>

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

### <span data-ttu-id="8a0a4-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8a0a4-129">-ResourceId</span></span>
<span data-ttu-id="8a0a4-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8a0a4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a0a4-131">-Confirm</span></span>
<span data-ttu-id="8a0a4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a0a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a0a4-133">-WhatIf</span></span>
<span data-ttu-id="8a0a4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a0a4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a0a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0a4-136">CommonParameters</span></span>
<span data-ttu-id="8a0a4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a0a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0a4-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a0a4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0a4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a0a4-139">INPUTS</span></span>

### <span data-ttu-id="8a0a4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8a0a4-140">System.String</span></span>

### <span data-ttu-id="8a0a4-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="8a0a4-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="8a0a4-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8a0a4-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8a0a4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a0a4-143">OUTPUTS</span></span>

### <span data-ttu-id="8a0a4-144">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="8a0a4-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="8a0a4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a0a4-145">NOTES</span></span>
<span data-ttu-id="8a0a4-146">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="8a0a4-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8a0a4-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a0a4-147">RELATED LINKS</span></span>

<span data-ttu-id="8a0a4-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="8a0a4-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

