---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 581f3c24c8c195b1cafc4962d1c6319418cc07f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589336"
---
# <span data-ttu-id="3ef0a-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef0a-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="3ef0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ef0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef0a-103">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="3ef0a-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ef0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ef0a-104">SYNTAX</span></span>

### <span data-ttu-id="3ef0a-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ef0a-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef0a-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ef0a-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef0a-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3ef0a-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ef0a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ef0a-108">DESCRIPTION</span></span>
<span data-ttu-id="3ef0a-109">**Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet 'ı bir diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="3ef0a-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3ef0a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ef0a-110">EXAMPLES</span></span>

### <span data-ttu-id="3ef0a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3ef0a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="3ef0a-112">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="3ef0a-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3ef0a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ef0a-113">PARAMETERS</span></span>

### <span data-ttu-id="3ef0a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="3ef0a-114">-AsJob</span></span>
<span data-ttu-id="3ef0a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3ef0a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ef0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef0a-116">-DefaultProfile</span></span>
<span data-ttu-id="3ef0a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef0a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ef0a-118">-InputObject</span></span>
<span data-ttu-id="3ef0a-119">Hizmet veri yolu GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="3ef0a-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef0a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ef0a-120">-Name</span></span>
<span data-ttu-id="3ef0a-121">Diğer ad (GeoDR) adı</span><span class="sxs-lookup"><span data-stu-id="3ef0a-121">Alias (GeoDR) Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef0a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3ef0a-122">-Namespace</span></span>
<span data-ttu-id="3ef0a-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="3ef0a-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef0a-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3ef0a-124">-PassThru</span></span>
<span data-ttu-id="3ef0a-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3ef0a-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3ef0a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef0a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ef0a-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3ef0a-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef0a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3ef0a-129">-ResourceId</span></span>
<span data-ttu-id="3ef0a-130">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3ef0a-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef0a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="3ef0a-131">-Confirm</span></span>
<span data-ttu-id="3ef0a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ef0a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef0a-133">-WhatIf</span></span>
<span data-ttu-id="3ef0a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ef0a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ef0a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef0a-136">CommonParameters</span></span>
<span data-ttu-id="3ef0a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef0a-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef0a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef0a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ef0a-139">INPUTS</span></span>

### <span data-ttu-id="3ef0a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3ef0a-140">System.String</span></span>

### <span data-ttu-id="3ef0a-141">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3ef0a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="3ef0a-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ef0a-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3ef0a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ef0a-143">OUTPUTS</span></span>

### <span data-ttu-id="3ef0a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ef0a-144">System.Boolean</span></span>

## <span data-ttu-id="3ef0a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ef0a-145">NOTES</span></span>

## <span data-ttu-id="3ef0a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ef0a-146">RELATED LINKS</span></span>
