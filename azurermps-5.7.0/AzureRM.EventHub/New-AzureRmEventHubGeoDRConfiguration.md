---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: feeb47a1db28debfcfeb4e5d61c22e15db66b799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588212"
---
# <span data-ttu-id="e0f68-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0f68-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="e0f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f68-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f68-103">Yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="e0f68-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0f68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0f68-104">SYNTAX</span></span>

### <span data-ttu-id="e0f68-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0f68-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f68-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e0f68-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f68-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f68-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0f68-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0f68-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f68-109">**Yeni-AzureRmEventHubGeoDRConfiguration** cmdlet 'i yeni bir diğer ad (olağanüstü durum kurtarma yapılandırması) oluşturur</span><span class="sxs-lookup"><span data-stu-id="e0f68-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="e0f68-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0f68-110">EXAMPLES</span></span>

### <span data-ttu-id="e0f68-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0f68-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="e0f68-112">"SampleNamespace_Secondary" ikincil ad alanıyla "SampleNamespace_Primary" birincil ad alanıyla "SampleDRCongifName" diğer adını oluşturur</span><span class="sxs-lookup"><span data-stu-id="e0f68-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="e0f68-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0f68-113">PARAMETERS</span></span>

### <span data-ttu-id="e0f68-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="e0f68-114">-AlternateName</span></span>
<span data-ttu-id="e0f68-115">DR yapılandırma adı birincil ad alanıyla aynı olduğunda AlternateName gereklidir</span><span class="sxs-lookup"><span data-stu-id="e0f68-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f68-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="e0f68-116">-AsJob</span></span>
<span data-ttu-id="e0f68-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e0f68-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0f68-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f68-118">-DefaultProfile</span></span>
<span data-ttu-id="e0f68-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0f68-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0f68-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0f68-120">-InputObject</span></span>
<span data-ttu-id="e0f68-121">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="e0f68-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f68-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0f68-122">-Name</span></span>
<span data-ttu-id="e0f68-123">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="e0f68-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f68-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e0f68-124">-Namespace</span></span>
<span data-ttu-id="e0f68-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="e0f68-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f68-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="e0f68-126">-PartnerNamespace</span></span>
<span data-ttu-id="e0f68-127">DR yapılandırma partneri ad alanı</span><span class="sxs-lookup"><span data-stu-id="e0f68-127">DR Configuration PartnerNamespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f68-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f68-128">-ResourceGroupName</span></span>
<span data-ttu-id="e0f68-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e0f68-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f68-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e0f68-130">-ResourceId</span></span>
<span data-ttu-id="e0f68-131">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e0f68-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f68-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0f68-132">-Confirm</span></span>
<span data-ttu-id="e0f68-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0f68-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f68-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f68-134">-WhatIf</span></span>
<span data-ttu-id="e0f68-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0f68-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0f68-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0f68-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f68-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f68-137">CommonParameters</span></span>
<span data-ttu-id="e0f68-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0f68-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e0f68-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f68-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f68-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0f68-140">INPUTS</span></span>

### <span data-ttu-id="e0f68-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e0f68-141">System.String</span></span>
<span data-ttu-id="e0f68-142">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e0f68-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="e0f68-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0f68-143">OUTPUTS</span></span>

### <span data-ttu-id="e0f68-144">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="e0f68-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="e0f68-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0f68-145">NOTES</span></span>

## <span data-ttu-id="e0f68-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0f68-146">RELATED LINKS</span></span>
