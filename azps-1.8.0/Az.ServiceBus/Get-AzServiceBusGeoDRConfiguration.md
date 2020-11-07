---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: fd87311c59c0889a57cb22eb08aba855e5c3b49c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759210"
---
# <span data-ttu-id="9e2b0-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e2b0-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="9e2b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2b0-103">Birincil veya ikincil ad alanı için diğer ad (olağanüstü durum kurtarma yapılandırması) alır</span><span class="sxs-lookup"><span data-stu-id="9e2b0-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="9e2b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e2b0-104">SYNTAX</span></span>

### <span data-ttu-id="9e2b0-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e2b0-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e2b0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9e2b0-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e2b0-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9e2b0-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e2b0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e2b0-108">DESCRIPTION</span></span>
<span data-ttu-id="9e2b0-109">Birincil veya ikincil ad alanı için **Get-AzServiceBusGeoDRConfiguration** (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="9e2b0-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="9e2b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e2b0-110">EXAMPLES</span></span>

### <span data-ttu-id="9e2b0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e2b0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="9e2b0-112">"SampleNamespace_Primary" birincil ad alanı için "SampleDRCongifName" diğer adını alır</span><span class="sxs-lookup"><span data-stu-id="9e2b0-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="9e2b0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e2b0-113">PARAMETERS</span></span>

### <span data-ttu-id="9e2b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2b0-114">-DefaultProfile</span></span>
<span data-ttu-id="9e2b0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e2b0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e2b0-116">-InputObject</span></span>
<span data-ttu-id="9e2b0-117">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="9e2b0-117">Namespace Object</span></span>

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

### <span data-ttu-id="9e2b0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e2b0-118">-Name</span></span>
<span data-ttu-id="9e2b0-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="9e2b0-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="9e2b0-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e2b0-120">-Namespace</span></span>
<span data-ttu-id="9e2b0-121">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="9e2b0-121">Namespace Name</span></span>

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

### <span data-ttu-id="9e2b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e2b0-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9e2b0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9e2b0-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9e2b0-124">-ResourceId</span></span>
<span data-ttu-id="9e2b0-125">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9e2b0-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="9e2b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2b0-126">CommonParameters</span></span>
<span data-ttu-id="9e2b0-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2b0-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2b0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2b0-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e2b0-129">INPUTS</span></span>

### <span data-ttu-id="9e2b0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9e2b0-130">System.String</span></span>

### <span data-ttu-id="9e2b0-131">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9e2b0-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9e2b0-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e2b0-132">OUTPUTS</span></span>

### <span data-ttu-id="9e2b0-133">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9e2b0-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="9e2b0-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e2b0-134">NOTES</span></span>

## <span data-ttu-id="9e2b0-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e2b0-135">RELATED LINKS</span></span>
