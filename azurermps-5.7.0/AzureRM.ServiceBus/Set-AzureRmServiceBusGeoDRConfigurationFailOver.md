---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 1a6fc5bca4c31afe08591190c111649495555cde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591603"
---
# <span data-ttu-id="fa197-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="fa197-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="fa197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa197-102">SYNOPSIS</span></span>
<span data-ttu-id="fa197-103">COĞRAFI DR yük devretmesini başlatır ve diğer adı ikincil ad alanına işaret edecek şekilde yeniden yapılandırın</span><span class="sxs-lookup"><span data-stu-id="fa197-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa197-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa197-104">SYNTAX</span></span>

### <span data-ttu-id="fa197-105">GeoDRBreakPairFailOverPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa197-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa197-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa197-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa197-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fa197-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa197-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa197-108">DESCRIPTION</span></span>
<span data-ttu-id="fa197-109">**Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet 'ı, coğrafi Dr yük devretmesini</span><span class="sxs-lookup"><span data-stu-id="fa197-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="fa197-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa197-110">EXAMPLES</span></span>

### <span data-ttu-id="fa197-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa197-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="fa197-112">"SampleDRCongifName" diğer adı üzerinden yük devretmeyi çağırır, yeniden yapılandırır ve "SampleNamespace_Secondary" Ikincil ad alanını işaret edin</span><span class="sxs-lookup"><span data-stu-id="fa197-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="fa197-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa197-113">PARAMETERS</span></span>

### <span data-ttu-id="fa197-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa197-114">-DefaultProfile</span></span>
<span data-ttu-id="fa197-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa197-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa197-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa197-116">-InputObject</span></span>
<span data-ttu-id="fa197-117">Hizmet veri yolu GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="fa197-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="fa197-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa197-118">-Name</span></span>
<span data-ttu-id="fa197-119">DR yapılandırma adı-diğer ad</span><span class="sxs-lookup"><span data-stu-id="fa197-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="fa197-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fa197-120">-Namespace</span></span>
<span data-ttu-id="fa197-121">Ad alanı adı-Ikincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="fa197-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="fa197-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fa197-122">-PassThru</span></span>
<span data-ttu-id="fa197-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa197-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa197-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fa197-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa197-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa197-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa197-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fa197-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fa197-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fa197-127">-ResourceId</span></span>
<span data-ttu-id="fa197-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fa197-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="fa197-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa197-129">-Confirm</span></span>
<span data-ttu-id="fa197-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa197-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa197-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa197-131">-WhatIf</span></span>
<span data-ttu-id="fa197-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa197-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa197-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa197-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa197-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa197-134">CommonParameters</span></span>
<span data-ttu-id="fa197-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa197-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fa197-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa197-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa197-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa197-137">INPUTS</span></span>

### <span data-ttu-id="fa197-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fa197-138">System.String</span></span>
<span data-ttu-id="fa197-139">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fa197-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="fa197-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa197-140">OUTPUTS</span></span>

### <span data-ttu-id="fa197-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa197-141">System.Boolean</span></span>


## <span data-ttu-id="fa197-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa197-142">NOTES</span></span>

## <span data-ttu-id="fa197-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa197-143">RELATED LINKS</span></span>
