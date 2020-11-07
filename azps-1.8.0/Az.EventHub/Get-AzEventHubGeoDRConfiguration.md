---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: a4cb60c224c440654854cff66434be1d224e8d50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760848"
---
# <span data-ttu-id="6a4c6-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a4c6-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="6a4c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a4c6-103">Birincil veya ikincil ad alanı için diğer ad (olağanüstü durum kurtarma yapılandırması) alır</span><span class="sxs-lookup"><span data-stu-id="6a4c6-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="6a4c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a4c6-104">SYNTAX</span></span>

### <span data-ttu-id="6a4c6-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a4c6-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a4c6-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6a4c6-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a4c6-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6a4c6-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a4c6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a4c6-108">DESCRIPTION</span></span>
<span data-ttu-id="6a4c6-109">Birincil veya ikincil ad alanı için **Get-AzEventHubGeoDRConfiguration** diğer ad (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="6a4c6-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="6a4c6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a4c6-110">EXAMPLES</span></span>

### <span data-ttu-id="6a4c6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a4c6-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="6a4c6-112">"SampleNamespace_Primary" birincil ad alanı için "SampleDRCongifName" diğer adını alır</span><span class="sxs-lookup"><span data-stu-id="6a4c6-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="6a4c6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a4c6-113">PARAMETERS</span></span>

### <span data-ttu-id="6a4c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a4c6-114">-DefaultProfile</span></span>
<span data-ttu-id="6a4c6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a4c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a4c6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a4c6-116">-InputObject</span></span>
<span data-ttu-id="6a4c6-117">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="6a4c6-117">Namespace Object</span></span>

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

### <span data-ttu-id="6a4c6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a4c6-118">-Name</span></span>
<span data-ttu-id="6a4c6-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="6a4c6-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="6a4c6-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a4c6-120">-Namespace</span></span>
<span data-ttu-id="6a4c6-121">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="6a4c6-121">Namespace Name</span></span>

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

### <span data-ttu-id="6a4c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a4c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a4c6-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6a4c6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="6a4c6-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6a4c6-124">-ResourceId</span></span>
<span data-ttu-id="6a4c6-125">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6a4c6-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="6a4c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a4c6-126">CommonParameters</span></span>
<span data-ttu-id="6a4c6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a4c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a4c6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a4c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a4c6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a4c6-129">INPUTS</span></span>

### <span data-ttu-id="6a4c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6a4c6-130">System.String</span></span>

### <span data-ttu-id="6a4c6-131">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="6a4c6-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="6a4c6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a4c6-132">OUTPUTS</span></span>

### <span data-ttu-id="6a4c6-133">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="6a4c6-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="6a4c6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a4c6-134">NOTES</span></span>

## <span data-ttu-id="6a4c6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a4c6-135">RELATED LINKS</span></span>
