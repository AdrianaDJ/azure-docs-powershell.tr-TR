---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273963"
---
# <span data-ttu-id="08ddd-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="08ddd-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="08ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="08ddd-103">Yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="08ddd-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="08ddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08ddd-104">SYNTAX</span></span>

### <span data-ttu-id="08ddd-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="08ddd-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ddd-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="08ddd-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ddd-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ddd-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08ddd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="08ddd-108">DESCRIPTION</span></span>
<span data-ttu-id="08ddd-109">**New-AzServiceBusGeoDRConfiguration** cmdlet 'i yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="08ddd-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="08ddd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08ddd-110">EXAMPLES</span></span>

### <span data-ttu-id="08ddd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08ddd-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="08ddd-112">"SampleNamespace_Secondary" ikincil ad alanı olan "SampleNamespace_Primary" birincil ad alanına sahip "SampleDRConfigName" diğer adını oluşturur</span><span class="sxs-lookup"><span data-stu-id="08ddd-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="08ddd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08ddd-113">PARAMETERS</span></span>

### <span data-ttu-id="08ddd-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="08ddd-114">-AlternateName</span></span>
<span data-ttu-id="08ddd-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="08ddd-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ddd-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="08ddd-116">-AsJob</span></span>
<span data-ttu-id="08ddd-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="08ddd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08ddd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ddd-118">-DefaultProfile</span></span>
<span data-ttu-id="08ddd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08ddd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08ddd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08ddd-120">-InputObject</span></span>
<span data-ttu-id="08ddd-121">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="08ddd-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08ddd-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="08ddd-122">-Name</span></span>
<span data-ttu-id="08ddd-123">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="08ddd-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ddd-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="08ddd-124">-Namespace</span></span>
<span data-ttu-id="08ddd-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="08ddd-125">Namespace Name</span></span>

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

### <span data-ttu-id="08ddd-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="08ddd-126">-PartnerNamespace</span></span>
<span data-ttu-id="08ddd-127">DR yapılandırma partneri ad alanı (PARTNERIN adalanı</span><span class="sxs-lookup"><span data-stu-id="08ddd-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ddd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ddd-128">-ResourceGroupName</span></span>
<span data-ttu-id="08ddd-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="08ddd-129">Resource Group Name</span></span>

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

### <span data-ttu-id="08ddd-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="08ddd-130">-ResourceId</span></span>
<span data-ttu-id="08ddd-131">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="08ddd-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ddd-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="08ddd-132">-Confirm</span></span>
<span data-ttu-id="08ddd-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08ddd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ddd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ddd-134">-WhatIf</span></span>
<span data-ttu-id="08ddd-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08ddd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08ddd-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08ddd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ddd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ddd-137">CommonParameters</span></span>
<span data-ttu-id="08ddd-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08ddd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ddd-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ddd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ddd-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08ddd-140">INPUTS</span></span>

### <span data-ttu-id="08ddd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="08ddd-141">System.String</span></span>

### <span data-ttu-id="08ddd-142">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="08ddd-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="08ddd-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08ddd-143">OUTPUTS</span></span>

### <span data-ttu-id="08ddd-144">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="08ddd-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="08ddd-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08ddd-145">NOTES</span></span>

## <span data-ttu-id="08ddd-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08ddd-146">RELATED LINKS</span></span>
