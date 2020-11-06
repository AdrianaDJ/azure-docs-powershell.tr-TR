---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588768"
---
# <span data-ttu-id="fe0da-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe0da-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="fe0da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0da-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0da-103">Birincil veya ikincil ad alanı için diğer ad (olağanüstü durum kurtarma yapılandırması) alır</span><span class="sxs-lookup"><span data-stu-id="fe0da-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe0da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe0da-104">SYNTAX</span></span>

### <span data-ttu-id="fe0da-105">GeoDRPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe0da-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe0da-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe0da-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe0da-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fe0da-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe0da-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe0da-108">DESCRIPTION</span></span>
<span data-ttu-id="fe0da-109">Birincil veya ikincil ad alanı için **Get-AzureRmServiceBusGeoDRConfiguration** diğer adı (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="fe0da-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="fe0da-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe0da-110">EXAMPLES</span></span>

### <span data-ttu-id="fe0da-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fe0da-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="fe0da-112">"SampleNamespace_Primary" birincil ad alanı için "SampleDRCongifName" diğer adını alır</span><span class="sxs-lookup"><span data-stu-id="fe0da-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="fe0da-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe0da-113">PARAMETERS</span></span>

### <span data-ttu-id="fe0da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0da-114">-DefaultProfile</span></span>
<span data-ttu-id="fe0da-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe0da-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe0da-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe0da-116">-InputObject</span></span>
<span data-ttu-id="fe0da-117">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="fe0da-117">Namespace Object</span></span>

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

### <span data-ttu-id="fe0da-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe0da-118">-Name</span></span>
<span data-ttu-id="fe0da-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="fe0da-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0da-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fe0da-120">-Namespace</span></span>
<span data-ttu-id="fe0da-121">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="fe0da-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0da-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe0da-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fe0da-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0da-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fe0da-124">-ResourceId</span></span>
<span data-ttu-id="fe0da-125">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fe0da-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0da-126">CommonParameters</span></span>
<span data-ttu-id="fe0da-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe0da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fe0da-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0da-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0da-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe0da-129">INPUTS</span></span>

### <span data-ttu-id="fe0da-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fe0da-130">System.String</span></span>
<span data-ttu-id="fe0da-131">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fe0da-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="fe0da-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe0da-132">OUTPUTS</span></span>

### <span data-ttu-id="fe0da-133">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fe0da-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="fe0da-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe0da-134">NOTES</span></span>

## <span data-ttu-id="fe0da-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe0da-135">RELATED LINKS</span></span>
