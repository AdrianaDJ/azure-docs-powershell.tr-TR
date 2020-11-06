---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 9c5fe091e5e218c4e70ef1486f1211bc0be7894b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591607"
---
# <span data-ttu-id="0d304-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d304-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="0d304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d304-102">SYNOPSIS</span></span>
<span data-ttu-id="0d304-103">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="0d304-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d304-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d304-104">SYNTAX</span></span>

### <span data-ttu-id="0d304-105">GeoDRBreakPairFailOverPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d304-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d304-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0d304-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d304-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0d304-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d304-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d304-108">DESCRIPTION</span></span>
<span data-ttu-id="0d304-109">**Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet 'ı bir diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="0d304-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0d304-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d304-110">EXAMPLES</span></span>

### <span data-ttu-id="0d304-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0d304-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="0d304-112">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="0d304-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0d304-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d304-113">PARAMETERS</span></span>

### <span data-ttu-id="0d304-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0d304-114">-AsJob</span></span>
<span data-ttu-id="0d304-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0d304-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d304-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d304-116">-DefaultProfile</span></span>
<span data-ttu-id="0d304-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d304-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d304-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d304-118">-InputObject</span></span>
<span data-ttu-id="0d304-119">Hizmet veri yolu GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="0d304-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d304-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d304-120">-Name</span></span>
<span data-ttu-id="0d304-121">Diğer ad (GeoDR) adı</span><span class="sxs-lookup"><span data-stu-id="0d304-121">Alias (GeoDR) Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d304-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0d304-122">-Namespace</span></span>
<span data-ttu-id="0d304-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="0d304-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d304-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0d304-124">-PassThru</span></span>
<span data-ttu-id="0d304-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0d304-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d304-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0d304-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d304-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d304-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d304-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0d304-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d304-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0d304-129">-ResourceId</span></span>
<span data-ttu-id="0d304-130">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0d304-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d304-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d304-131">-Confirm</span></span>
<span data-ttu-id="0d304-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d304-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d304-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d304-133">-WhatIf</span></span>
<span data-ttu-id="0d304-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d304-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d304-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d304-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d304-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d304-136">CommonParameters</span></span>
<span data-ttu-id="0d304-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d304-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0d304-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d304-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d304-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d304-139">INPUTS</span></span>

### <span data-ttu-id="0d304-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0d304-140">System.String</span></span>
<span data-ttu-id="0d304-141">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0d304-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="0d304-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d304-142">OUTPUTS</span></span>

### <span data-ttu-id="0d304-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d304-143">System.Boolean</span></span>


## <span data-ttu-id="0d304-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d304-144">NOTES</span></span>

## <span data-ttu-id="0d304-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d304-145">RELATED LINKS</span></span>
