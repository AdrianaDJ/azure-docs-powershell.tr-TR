---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4e6426b00a05568cff5b0fe1c153dcc41b36ed6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933215"
---
# <span data-ttu-id="6850a-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="6850a-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="6850a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6850a-102">SYNOPSIS</span></span>
<span data-ttu-id="6850a-103">COĞRAFI DR yük devretmesini başlatır ve diğer adı ikincil ad alanına işaret edecek şekilde yeniden yapılandırın</span><span class="sxs-lookup"><span data-stu-id="6850a-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="6850a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6850a-104">SYNTAX</span></span>

### <span data-ttu-id="6850a-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6850a-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6850a-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6850a-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6850a-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6850a-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6850a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6850a-108">DESCRIPTION</span></span>
<span data-ttu-id="6850a-109">**Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet 'ı, coğrafi</span><span class="sxs-lookup"><span data-stu-id="6850a-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="6850a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6850a-110">EXAMPLES</span></span>

### <span data-ttu-id="6850a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6850a-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="6850a-112">"SampleDRConfigName" diğer adı üzerinden yük devretmeyi çağırır, yeniden yapılandırır ve "SampleNamespace_Secondary" Ikincil ad alanını işaret eder</span><span class="sxs-lookup"><span data-stu-id="6850a-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="6850a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6850a-113">PARAMETERS</span></span>

### <span data-ttu-id="6850a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6850a-114">-DefaultProfile</span></span>
<span data-ttu-id="6850a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6850a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6850a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6850a-116">-InputObject</span></span>
<span data-ttu-id="6850a-117">Hizmet veri yolu GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="6850a-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="6850a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6850a-118">-Name</span></span>
<span data-ttu-id="6850a-119">DR yapılandırma adı-diğer ad</span><span class="sxs-lookup"><span data-stu-id="6850a-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="6850a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6850a-120">-Namespace</span></span>
<span data-ttu-id="6850a-121">Ad alanı adı-Ikincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="6850a-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="6850a-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6850a-122">-PassThru</span></span>
<span data-ttu-id="6850a-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6850a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6850a-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6850a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6850a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6850a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6850a-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6850a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6850a-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6850a-127">-ResourceId</span></span>
<span data-ttu-id="6850a-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6850a-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="6850a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6850a-129">-Confirm</span></span>
<span data-ttu-id="6850a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6850a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6850a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6850a-131">-WhatIf</span></span>
<span data-ttu-id="6850a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6850a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6850a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6850a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6850a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6850a-134">CommonParameters</span></span>
<span data-ttu-id="6850a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6850a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6850a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6850a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6850a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6850a-137">INPUTS</span></span>

### <span data-ttu-id="6850a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6850a-138">System.String</span></span>

### <span data-ttu-id="6850a-139">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6850a-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="6850a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6850a-140">OUTPUTS</span></span>

### <span data-ttu-id="6850a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6850a-141">System.Boolean</span></span>

## <span data-ttu-id="6850a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6850a-142">NOTES</span></span>

## <span data-ttu-id="6850a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6850a-143">RELATED LINKS</span></span>
