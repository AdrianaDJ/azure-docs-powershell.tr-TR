---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e2f1edfa0d1b5fa081754457fa3fc53f310eb345
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762894"
---
# <span data-ttu-id="dd9a1-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd9a1-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="dd9a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9a1-103">Yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="dd9a1-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd9a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd9a1-104">SYNTAX</span></span>

### <span data-ttu-id="dd9a1-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd9a1-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd9a1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd9a1-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd9a1-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd9a1-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd9a1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd9a1-108">DESCRIPTION</span></span>
<span data-ttu-id="dd9a1-109">**Yeni-AzureRmServiceBusGeoDRConfiguration** cmdlet 'i yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="dd9a1-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="dd9a1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd9a1-110">EXAMPLES</span></span>

### <span data-ttu-id="dd9a1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd9a1-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="dd9a1-112">"SampleNamespace_Secondary" ikincil ad alanıyla "SampleNamespace_Primary" birincil ad alanıyla "SampleDRCongifName" diğer adını oluşturur</span><span class="sxs-lookup"><span data-stu-id="dd9a1-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="dd9a1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd9a1-113">PARAMETERS</span></span>

### <span data-ttu-id="dd9a1-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="dd9a1-114">-AlternateName</span></span>
<span data-ttu-id="dd9a1-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="dd9a1-115">AlternateName</span></span>

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

### <span data-ttu-id="dd9a1-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="dd9a1-116">-AsJob</span></span>
<span data-ttu-id="dd9a1-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dd9a1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd9a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9a1-118">-DefaultProfile</span></span>
<span data-ttu-id="dd9a1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd9a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd9a1-120">-InputObject</span></span>
<span data-ttu-id="dd9a1-121">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="dd9a1-121">Namespace Object</span></span>

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

### <span data-ttu-id="dd9a1-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd9a1-122">-Name</span></span>
<span data-ttu-id="dd9a1-123">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="dd9a1-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="dd9a1-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd9a1-124">-Namespace</span></span>
<span data-ttu-id="dd9a1-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="dd9a1-125">Namespace Name</span></span>

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

### <span data-ttu-id="dd9a1-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="dd9a1-126">-PartnerNamespace</span></span>
<span data-ttu-id="dd9a1-127">DR yapılandırma partneri ad alanı (PARTNERIN adalanı</span><span class="sxs-lookup"><span data-stu-id="dd9a1-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="dd9a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd9a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd9a1-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dd9a1-129">Resource Group Name</span></span>

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

### <span data-ttu-id="dd9a1-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dd9a1-130">-ResourceId</span></span>
<span data-ttu-id="dd9a1-131">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="dd9a1-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="dd9a1-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd9a1-132">-Confirm</span></span>
<span data-ttu-id="dd9a1-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd9a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd9a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd9a1-134">-WhatIf</span></span>
<span data-ttu-id="dd9a1-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd9a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd9a1-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd9a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd9a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9a1-137">CommonParameters</span></span>
<span data-ttu-id="dd9a1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd9a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9a1-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd9a1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9a1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd9a1-140">INPUTS</span></span>

### <span data-ttu-id="dd9a1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dd9a1-141">System.String</span></span>

### <span data-ttu-id="dd9a1-142">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="dd9a1-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="dd9a1-143">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd9a1-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dd9a1-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd9a1-144">OUTPUTS</span></span>

### <span data-ttu-id="dd9a1-145">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dd9a1-145">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="dd9a1-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd9a1-146">NOTES</span></span>

## <span data-ttu-id="dd9a1-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd9a1-147">RELATED LINKS</span></span>
