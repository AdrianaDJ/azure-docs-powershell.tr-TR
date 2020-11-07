---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 551cf0b883c2af2517240c31a3e633298087534b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759149"
---
# <span data-ttu-id="e048d-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="e048d-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="e048d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e048d-102">SYNOPSIS</span></span>
<span data-ttu-id="e048d-103">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="e048d-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="e048d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e048d-104">SYNTAX</span></span>

### <span data-ttu-id="e048d-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e048d-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e048d-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e048d-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e048d-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e048d-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e048d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e048d-108">DESCRIPTION</span></span>
<span data-ttu-id="e048d-109">**Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet 'ı kilitlenme kurtarması</span><span class="sxs-lookup"><span data-stu-id="e048d-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="e048d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e048d-110">EXAMPLES</span></span>

### <span data-ttu-id="e048d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e048d-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="e048d-112">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="e048d-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="e048d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e048d-113">PARAMETERS</span></span>

### <span data-ttu-id="e048d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e048d-114">-DefaultProfile</span></span>
<span data-ttu-id="e048d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e048d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e048d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e048d-116">-InputObject</span></span>
<span data-ttu-id="e048d-117">Hizmet veri yolu GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="e048d-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="e048d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e048d-118">-Name</span></span>
<span data-ttu-id="e048d-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="e048d-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="e048d-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e048d-120">-Namespace</span></span>
<span data-ttu-id="e048d-121">Ad alanı adı-birincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="e048d-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="e048d-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e048d-122">-PassThru</span></span>
<span data-ttu-id="e048d-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e048d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e048d-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e048d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e048d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e048d-125">-ResourceGroupName</span></span>
<span data-ttu-id="e048d-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e048d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e048d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e048d-127">-ResourceId</span></span>
<span data-ttu-id="e048d-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e048d-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="e048d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e048d-129">-Confirm</span></span>
<span data-ttu-id="e048d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e048d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e048d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e048d-131">-WhatIf</span></span>
<span data-ttu-id="e048d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e048d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e048d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e048d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e048d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e048d-134">CommonParameters</span></span>
<span data-ttu-id="e048d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e048d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e048d-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e048d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e048d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e048d-137">INPUTS</span></span>

### <span data-ttu-id="e048d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e048d-138">System.String</span></span>

### <span data-ttu-id="e048d-139">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e048d-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="e048d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e048d-140">OUTPUTS</span></span>

### <span data-ttu-id="e048d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e048d-141">System.Boolean</span></span>

## <span data-ttu-id="e048d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e048d-142">NOTES</span></span>

## <span data-ttu-id="e048d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e048d-143">RELATED LINKS</span></span>