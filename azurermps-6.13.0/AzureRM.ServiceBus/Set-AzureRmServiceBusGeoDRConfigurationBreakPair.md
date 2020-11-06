---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: a12f22260ce8ee5412cd17ddfa420a7d23f82008
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590025"
---
# <span data-ttu-id="ec849-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="ec849-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="ec849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec849-102">SYNOPSIS</span></span>
<span data-ttu-id="ec849-103">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="ec849-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec849-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec849-104">SYNTAX</span></span>

### <span data-ttu-id="ec849-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec849-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec849-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ec849-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec849-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ec849-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec849-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec849-108">DESCRIPTION</span></span>
<span data-ttu-id="ec849-109">**Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet 'ı kilitlenme kurtarması</span><span class="sxs-lookup"><span data-stu-id="ec849-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="ec849-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec849-110">EXAMPLES</span></span>

### <span data-ttu-id="ec849-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec849-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="ec849-112">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="ec849-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="ec849-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec849-113">PARAMETERS</span></span>

### <span data-ttu-id="ec849-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec849-114">-DefaultProfile</span></span>
<span data-ttu-id="ec849-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec849-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec849-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec849-116">-InputObject</span></span>
<span data-ttu-id="ec849-117">Hizmet veri yolu GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="ec849-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="ec849-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec849-118">-Name</span></span>
<span data-ttu-id="ec849-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="ec849-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="ec849-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec849-120">-Namespace</span></span>
<span data-ttu-id="ec849-121">Ad alanı adı-birincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="ec849-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="ec849-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ec849-122">-PassThru</span></span>
<span data-ttu-id="ec849-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec849-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec849-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ec849-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec849-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec849-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec849-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ec849-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec849-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ec849-127">-ResourceId</span></span>
<span data-ttu-id="ec849-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ec849-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="ec849-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec849-129">-Confirm</span></span>
<span data-ttu-id="ec849-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec849-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec849-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec849-131">-WhatIf</span></span>
<span data-ttu-id="ec849-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec849-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec849-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec849-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec849-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec849-134">CommonParameters</span></span>
<span data-ttu-id="ec849-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec849-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec849-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec849-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec849-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec849-137">INPUTS</span></span>

### <span data-ttu-id="ec849-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ec849-138">System.String</span></span>

### <span data-ttu-id="ec849-139">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ec849-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="ec849-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ec849-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ec849-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec849-141">OUTPUTS</span></span>

### <span data-ttu-id="ec849-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec849-142">System.Boolean</span></span>

## <span data-ttu-id="ec849-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec849-143">NOTES</span></span>

## <span data-ttu-id="ec849-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec849-144">RELATED LINKS</span></span>
