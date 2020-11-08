---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275687"
---
# <span data-ttu-id="b4e54-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b4e54-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="b4e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e54-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e54-103">Belirli bir ad alanı veya sıra veya konu veya diğer ad (GeoDR yapılandırmaları) için belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="b4e54-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="b4e54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4e54-104">SYNTAX</span></span>

### <span data-ttu-id="b4e54-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4e54-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4e54-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e54-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4e54-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e54-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4e54-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e54-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e54-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4e54-109">DESCRIPTION</span></span>
<span data-ttu-id="b4e54-110">**Get-AzServiceBusAuthorizationRule** cmdlet 'i, verilen ad alanında veya kuyrukta veya konuda (Geodr yapılandırmaları) belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="b4e54-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="b4e54-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4e54-111">EXAMPLES</span></span>

### <span data-ttu-id="b4e54-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4e54-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="b4e54-113">Belirtilen ad alanı için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b4e54-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="b4e54-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b4e54-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="b4e54-115">Belirtilen bir sıranın belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b4e54-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="b4e54-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b4e54-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="b4e54-117">Belirtilen bir konu için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b4e54-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="b4e54-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="b4e54-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="b4e54-119">Belirtilen ad alanı ve diğer ad için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b4e54-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="b4e54-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4e54-120">PARAMETERS</span></span>

### <span data-ttu-id="b4e54-121">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="b4e54-121">-AliasName</span></span>
<span data-ttu-id="b4e54-122">GeoDR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="b4e54-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="b4e54-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e54-123">-DefaultProfile</span></span>
<span data-ttu-id="b4e54-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4e54-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e54-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4e54-125">-Name</span></span>
<span data-ttu-id="b4e54-126">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="b4e54-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b4e54-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b4e54-127">-Namespace</span></span>
<span data-ttu-id="b4e54-128">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b4e54-128">Namespace Name</span></span>

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

### <span data-ttu-id="b4e54-129">-Sıra</span><span class="sxs-lookup"><span data-stu-id="b4e54-129">-Queue</span></span>
<span data-ttu-id="b4e54-130">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="b4e54-130">Queue Name</span></span>

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

### <span data-ttu-id="b4e54-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e54-131">-ResourceGroupName</span></span>
<span data-ttu-id="b4e54-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b4e54-132">Resource Group Name</span></span>

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

### <span data-ttu-id="b4e54-133">-Konu</span><span class="sxs-lookup"><span data-stu-id="b4e54-133">-Topic</span></span>
<span data-ttu-id="b4e54-134">Konu adı</span><span class="sxs-lookup"><span data-stu-id="b4e54-134">Topic Name</span></span>

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

### <span data-ttu-id="b4e54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e54-135">CommonParameters</span></span>
<span data-ttu-id="b4e54-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4e54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e54-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e54-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e54-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4e54-138">INPUTS</span></span>

### <span data-ttu-id="b4e54-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4e54-139">System.String</span></span>

## <span data-ttu-id="b4e54-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4e54-140">OUTPUTS</span></span>

### <span data-ttu-id="b4e54-141">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b4e54-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b4e54-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4e54-142">NOTES</span></span>

## <span data-ttu-id="b4e54-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4e54-143">RELATED LINKS</span></span>
