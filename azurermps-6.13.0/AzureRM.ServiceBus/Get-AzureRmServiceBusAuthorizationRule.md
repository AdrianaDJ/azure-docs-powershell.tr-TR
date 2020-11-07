---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 8c69ab59f539180c3146f01c7a5fce9907b40c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762090"
---
# <span data-ttu-id="f34de-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f34de-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f34de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f34de-102">SYNOPSIS</span></span>
<span data-ttu-id="f34de-103">Belirli bir ad alanı veya sıra veya konu veya diğer ad (GeoDR yapılandırmaları) için belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="f34de-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f34de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f34de-104">SYNTAX</span></span>

### <span data-ttu-id="f34de-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f34de-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f34de-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f34de-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f34de-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f34de-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f34de-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="f34de-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f34de-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f34de-109">DESCRIPTION</span></span>
<span data-ttu-id="f34de-110">**Get-AzureRmServiceBusAuthorizationRule** cmdlet 'i, verilen ad alanında veya kuyrukta veya konuda (Geodr yapılandırmaları) belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="f34de-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="f34de-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f34de-111">EXAMPLES</span></span>

### <span data-ttu-id="f34de-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f34de-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f34de-113">Belirtilen ad alanı için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f34de-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="f34de-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f34de-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f34de-115">Belirtilen bir sıranın belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f34de-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="f34de-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f34de-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f34de-117">Belirtilen bir konu için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f34de-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="f34de-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="f34de-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="f34de-119">Belirtilen ad alanı ve diğer ad için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f34de-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="f34de-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f34de-120">PARAMETERS</span></span>

### <span data-ttu-id="f34de-121">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="f34de-121">-AliasName</span></span>
<span data-ttu-id="f34de-122">GeoDR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="f34de-122">GeoDR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f34de-123">-DefaultProfile</span></span>
<span data-ttu-id="f34de-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f34de-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f34de-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="f34de-125">-Name</span></span>
<span data-ttu-id="f34de-126">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="f34de-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34de-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f34de-127">-Namespace</span></span>
<span data-ttu-id="f34de-128">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="f34de-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34de-129">-Sıra</span><span class="sxs-lookup"><span data-stu-id="f34de-129">-Queue</span></span>
<span data-ttu-id="f34de-130">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="f34de-130">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34de-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f34de-131">-ResourceGroupName</span></span>
<span data-ttu-id="f34de-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f34de-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34de-133">-Konu</span><span class="sxs-lookup"><span data-stu-id="f34de-133">-Topic</span></span>
<span data-ttu-id="f34de-134">Konu adı</span><span class="sxs-lookup"><span data-stu-id="f34de-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f34de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34de-135">CommonParameters</span></span>
<span data-ttu-id="f34de-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f34de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34de-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f34de-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34de-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f34de-138">INPUTS</span></span>

### <span data-ttu-id="f34de-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f34de-139">System.String</span></span>

## <span data-ttu-id="f34de-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f34de-140">OUTPUTS</span></span>

### <span data-ttu-id="f34de-141">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f34de-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f34de-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f34de-142">NOTES</span></span>

## <span data-ttu-id="f34de-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f34de-143">RELATED LINKS</span></span>
