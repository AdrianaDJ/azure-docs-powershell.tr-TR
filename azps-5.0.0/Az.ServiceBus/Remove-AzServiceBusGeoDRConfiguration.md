---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276540"
---
# <span data-ttu-id="59f4a-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="59f4a-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="59f4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="59f4a-103">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="59f4a-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="59f4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59f4a-104">SYNTAX</span></span>

### <span data-ttu-id="59f4a-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59f4a-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f4a-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59f4a-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f4a-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="59f4a-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f4a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59f4a-108">DESCRIPTION</span></span>
<span data-ttu-id="59f4a-109">**Remove-AzServiceBusGeoDRConfiguration** cmdlet 'ı bir diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="59f4a-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="59f4a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59f4a-110">EXAMPLES</span></span>

### <span data-ttu-id="59f4a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59f4a-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="59f4a-112">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="59f4a-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="59f4a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59f4a-113">PARAMETERS</span></span>

### <span data-ttu-id="59f4a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="59f4a-114">-AsJob</span></span>
<span data-ttu-id="59f4a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="59f4a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59f4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f4a-116">-DefaultProfile</span></span>
<span data-ttu-id="59f4a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59f4a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f4a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59f4a-118">-InputObject</span></span>
<span data-ttu-id="59f4a-119">Hizmet veri yolu GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="59f4a-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="59f4a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="59f4a-120">-Name</span></span>
<span data-ttu-id="59f4a-121">Diğer ad (GeoDR) adı</span><span class="sxs-lookup"><span data-stu-id="59f4a-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="59f4a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="59f4a-122">-Namespace</span></span>
<span data-ttu-id="59f4a-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="59f4a-123">Namespace Name</span></span>

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

### <span data-ttu-id="59f4a-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59f4a-124">-PassThru</span></span>
<span data-ttu-id="59f4a-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="59f4a-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59f4a-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="59f4a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59f4a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f4a-127">-ResourceGroupName</span></span>
<span data-ttu-id="59f4a-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="59f4a-128">Resource Group Name</span></span>

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

### <span data-ttu-id="59f4a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="59f4a-129">-ResourceId</span></span>
<span data-ttu-id="59f4a-130">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="59f4a-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="59f4a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="59f4a-131">-Confirm</span></span>
<span data-ttu-id="59f4a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59f4a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f4a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f4a-133">-WhatIf</span></span>
<span data-ttu-id="59f4a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f4a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f4a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59f4a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f4a-136">CommonParameters</span></span>
<span data-ttu-id="59f4a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59f4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f4a-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f4a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f4a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59f4a-139">INPUTS</span></span>

### <span data-ttu-id="59f4a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="59f4a-140">System.String</span></span>

### <span data-ttu-id="59f4a-141">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="59f4a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="59f4a-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59f4a-142">OUTPUTS</span></span>

### <span data-ttu-id="59f4a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59f4a-143">System.Boolean</span></span>

## <span data-ttu-id="59f4a-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59f4a-144">NOTES</span></span>

## <span data-ttu-id="59f4a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59f4a-145">RELATED LINKS</span></span>
