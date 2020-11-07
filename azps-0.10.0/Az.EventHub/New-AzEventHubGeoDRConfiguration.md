---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2c48ad3bda14775dd0535b63343d90f026bf614
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935881"
---
# <span data-ttu-id="44ef5-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="44ef5-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="44ef5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="44ef5-103">Yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="44ef5-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="44ef5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44ef5-104">SYNTAX</span></span>

### <span data-ttu-id="44ef5-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44ef5-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44ef5-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44ef5-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44ef5-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44ef5-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44ef5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="44ef5-108">DESCRIPTION</span></span>
<span data-ttu-id="44ef5-109">**Yeni-AzEventHubGeoDRConfiguration** cmdlet 'i yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="44ef5-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="44ef5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44ef5-110">EXAMPLES</span></span>

### <span data-ttu-id="44ef5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44ef5-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="44ef5-112">"SampleNamespace_Secondary" ikincil ad alanı olan "SampleNamespace_Primary" birincil ad alanına sahip "SampleDRConfigName" diğer adını oluşturur</span><span class="sxs-lookup"><span data-stu-id="44ef5-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="44ef5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44ef5-113">PARAMETERS</span></span>

### <span data-ttu-id="44ef5-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="44ef5-114">-AlternateName</span></span>
<span data-ttu-id="44ef5-115">DR yapılandırma adı birincil ad alanıyla aynı olduğunda AlternateName gereklidir</span><span class="sxs-lookup"><span data-stu-id="44ef5-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="44ef5-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="44ef5-116">-AsJob</span></span>
<span data-ttu-id="44ef5-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="44ef5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44ef5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ef5-118">-DefaultProfile</span></span>
<span data-ttu-id="44ef5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44ef5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ef5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44ef5-120">-InputObject</span></span>
<span data-ttu-id="44ef5-121">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="44ef5-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44ef5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="44ef5-122">-Name</span></span>
<span data-ttu-id="44ef5-123">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="44ef5-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="44ef5-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="44ef5-124">-Namespace</span></span>
<span data-ttu-id="44ef5-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="44ef5-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ef5-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="44ef5-126">-PartnerNamespace</span></span>
<span data-ttu-id="44ef5-127">DR yapılandırma partneri ad alanı</span><span class="sxs-lookup"><span data-stu-id="44ef5-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="44ef5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ef5-128">-ResourceGroupName</span></span>
<span data-ttu-id="44ef5-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="44ef5-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ef5-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="44ef5-130">-ResourceId</span></span>
<span data-ttu-id="44ef5-131">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="44ef5-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="44ef5-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="44ef5-132">-Confirm</span></span>
<span data-ttu-id="44ef5-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="44ef5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44ef5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ef5-134">-WhatIf</span></span>
<span data-ttu-id="44ef5-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44ef5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44ef5-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="44ef5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44ef5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ef5-137">CommonParameters</span></span>
<span data-ttu-id="44ef5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44ef5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ef5-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ef5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ef5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44ef5-140">INPUTS</span></span>

### <span data-ttu-id="44ef5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="44ef5-141">System.String</span></span>

### <span data-ttu-id="44ef5-142">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="44ef5-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="44ef5-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44ef5-143">OUTPUTS</span></span>

### <span data-ttu-id="44ef5-144">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="44ef5-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="44ef5-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44ef5-145">NOTES</span></span>

## <span data-ttu-id="44ef5-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44ef5-146">RELATED LINKS</span></span>
