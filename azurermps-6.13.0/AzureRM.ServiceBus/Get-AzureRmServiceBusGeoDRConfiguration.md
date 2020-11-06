---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 7d3635b33e96052c42ca77384d2f138af5cc0d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592733"
---
# <span data-ttu-id="bb350-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb350-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="bb350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb350-102">SYNOPSIS</span></span>
<span data-ttu-id="bb350-103">Birincil veya ikincil ad alanı için diğer ad (olağanüstü durum kurtarma yapılandırması) alır</span><span class="sxs-lookup"><span data-stu-id="bb350-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb350-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb350-104">SYNTAX</span></span>

### <span data-ttu-id="bb350-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb350-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb350-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb350-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb350-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bb350-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb350-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb350-108">DESCRIPTION</span></span>
<span data-ttu-id="bb350-109">Birincil veya ikincil ad alanı için **Get-AzureRmServiceBusGeoDRConfiguration** diğer adı (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="bb350-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="bb350-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb350-110">EXAMPLES</span></span>

### <span data-ttu-id="bb350-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb350-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="bb350-112">"SampleNamespace_Primary" birincil ad alanı için "SampleDRCongifName" diğer adını alır</span><span class="sxs-lookup"><span data-stu-id="bb350-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="bb350-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb350-113">PARAMETERS</span></span>

### <span data-ttu-id="bb350-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb350-114">-DefaultProfile</span></span>
<span data-ttu-id="bb350-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb350-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb350-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb350-116">-InputObject</span></span>
<span data-ttu-id="bb350-117">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="bb350-117">Namespace Object</span></span>

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

### <span data-ttu-id="bb350-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb350-118">-Name</span></span>
<span data-ttu-id="bb350-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="bb350-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="bb350-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb350-120">-Namespace</span></span>
<span data-ttu-id="bb350-121">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="bb350-121">Namespace Name</span></span>

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

### <span data-ttu-id="bb350-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb350-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb350-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bb350-123">Resource Group Name</span></span>

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

### <span data-ttu-id="bb350-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb350-124">-ResourceId</span></span>
<span data-ttu-id="bb350-125">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="bb350-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="bb350-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb350-126">CommonParameters</span></span>
<span data-ttu-id="bb350-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb350-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb350-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb350-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb350-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb350-129">INPUTS</span></span>

### <span data-ttu-id="bb350-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bb350-130">System.String</span></span>

### <span data-ttu-id="bb350-131">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bb350-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="bb350-132">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb350-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bb350-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb350-133">OUTPUTS</span></span>

### <span data-ttu-id="bb350-134">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bb350-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="bb350-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb350-135">NOTES</span></span>

## <span data-ttu-id="bb350-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb350-136">RELATED LINKS</span></span>
