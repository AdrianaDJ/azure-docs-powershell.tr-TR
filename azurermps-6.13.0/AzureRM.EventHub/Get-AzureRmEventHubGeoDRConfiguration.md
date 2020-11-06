---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589544"
---
# <span data-ttu-id="9f70b-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f70b-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="9f70b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f70b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f70b-103">Birincil veya ikincil ad alanı için diğer ad (olağanüstü durum kurtarma yapılandırması) alır</span><span class="sxs-lookup"><span data-stu-id="9f70b-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f70b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f70b-104">SYNTAX</span></span>

### <span data-ttu-id="9f70b-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f70b-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f70b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f70b-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f70b-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9f70b-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f70b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f70b-108">DESCRIPTION</span></span>
<span data-ttu-id="9f70b-109">**Get-AzureRmEventHubGeoDRConfiguration** , birincil veya ikincil ad alanı Için diğer ad (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="9f70b-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="9f70b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f70b-110">EXAMPLES</span></span>

### <span data-ttu-id="9f70b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9f70b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="9f70b-112">"SampleNamespace_Primary" birincil ad alanı için "SampleDRCongifName" diğer adını alır</span><span class="sxs-lookup"><span data-stu-id="9f70b-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="9f70b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f70b-113">PARAMETERS</span></span>

### <span data-ttu-id="9f70b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f70b-114">-DefaultProfile</span></span>
<span data-ttu-id="9f70b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f70b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f70b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f70b-116">-InputObject</span></span>
<span data-ttu-id="9f70b-117">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="9f70b-117">Namespace Object</span></span>

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

### <span data-ttu-id="9f70b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f70b-118">-Name</span></span>
<span data-ttu-id="9f70b-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="9f70b-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="9f70b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9f70b-120">-Namespace</span></span>
<span data-ttu-id="9f70b-121">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="9f70b-121">Namespace Name</span></span>

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

### <span data-ttu-id="9f70b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f70b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f70b-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9f70b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9f70b-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f70b-124">-ResourceId</span></span>
<span data-ttu-id="9f70b-125">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9f70b-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f70b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f70b-126">CommonParameters</span></span>
<span data-ttu-id="9f70b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f70b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f70b-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f70b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f70b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f70b-129">INPUTS</span></span>

### <span data-ttu-id="9f70b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9f70b-130">System.String</span></span>

### <span data-ttu-id="9f70b-131">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9f70b-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="9f70b-132">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9f70b-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9f70b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f70b-133">OUTPUTS</span></span>

### <span data-ttu-id="9f70b-134">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="9f70b-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="9f70b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f70b-135">NOTES</span></span>

## <span data-ttu-id="9f70b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f70b-136">RELATED LINKS</span></span>
