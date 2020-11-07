---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: c9d6e262acd20616cf070ab061b48a61ccfbba48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933248"
---
# <span data-ttu-id="a4ae1-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="a4ae1-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="a4ae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ae1-103">Verilen ad alanı veya sıra veya konu veya diğer ad (GeoDR yapılandırmaları) için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="a4ae1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4ae1-104">SYNTAX</span></span>

### <span data-ttu-id="a4ae1-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a4ae1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ae1-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ae1-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ae1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ae1-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ae1-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ae1-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4ae1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4ae1-109">DESCRIPTION</span></span>
<span data-ttu-id="a4ae1-110">**Get-AzServiceBusKey** cmdlet 'i, verilen ad alanı veya sıra veya konu veya diğer ad (Geodr yapılandırmaları) için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="a4ae1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4ae1-111">EXAMPLES</span></span>

### <span data-ttu-id="a4ae1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4ae1-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="a4ae1-113">Belirtilen ad alanına birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="a4ae1-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a4ae1-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="a4ae1-115">Belirtilen sıraya birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="a4ae1-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a4ae1-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="a4ae1-117">Belirtilen konuya birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="a4ae1-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a4ae1-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="a4ae1-119">Belirtilen ad alanı ve diğer ada birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="a4ae1-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4ae1-120">PARAMETERS</span></span>

### <span data-ttu-id="a4ae1-121">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="a4ae1-121">-AliasName</span></span>
<span data-ttu-id="a4ae1-122">Diğer ad</span><span class="sxs-lookup"><span data-stu-id="a4ae1-122">Alias Name</span></span>

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

### <span data-ttu-id="a4ae1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ae1-123">-DefaultProfile</span></span>
<span data-ttu-id="a4ae1-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ae1-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4ae1-125">-Name</span></span>
<span data-ttu-id="a4ae1-126">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="a4ae1-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ae1-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4ae1-127">-Namespace</span></span>
<span data-ttu-id="a4ae1-128">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="a4ae1-128">Namespace Name</span></span>

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

### <span data-ttu-id="a4ae1-129">-Sıra</span><span class="sxs-lookup"><span data-stu-id="a4ae1-129">-Queue</span></span>
<span data-ttu-id="a4ae1-130">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="a4ae1-130">Queue Name</span></span>

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

### <span data-ttu-id="a4ae1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ae1-131">-ResourceGroupName</span></span>
<span data-ttu-id="a4ae1-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a4ae1-132">Resource Group Name</span></span>

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

### <span data-ttu-id="a4ae1-133">-Konu</span><span class="sxs-lookup"><span data-stu-id="a4ae1-133">-Topic</span></span>
<span data-ttu-id="a4ae1-134">Konu adı</span><span class="sxs-lookup"><span data-stu-id="a4ae1-134">Topic Name</span></span>

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

### <span data-ttu-id="a4ae1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ae1-135">CommonParameters</span></span>
<span data-ttu-id="a4ae1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ae1-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ae1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ae1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4ae1-138">INPUTS</span></span>

### <span data-ttu-id="a4ae1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ae1-139">System.String</span></span>

## <span data-ttu-id="a4ae1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4ae1-140">OUTPUTS</span></span>

### <span data-ttu-id="a4ae1-141">Microsoft. Azure. Commands. ServiceBus. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a4ae1-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="a4ae1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4ae1-142">NOTES</span></span>

## <span data-ttu-id="a4ae1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4ae1-143">RELATED LINKS</span></span>
