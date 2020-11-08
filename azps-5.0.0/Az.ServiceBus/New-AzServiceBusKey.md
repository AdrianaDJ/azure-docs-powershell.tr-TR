---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275873"
---
# <span data-ttu-id="b5561-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="b5561-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="b5561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5561-102">SYNOPSIS</span></span>
<span data-ttu-id="b5561-103">Hizmet veri yolu ad alanı veya sıra veya konu için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="b5561-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5561-104">SYNTAX</span></span>

### <span data-ttu-id="b5561-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5561-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5561-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5561-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5561-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5561-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5561-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5561-108">DESCRIPTION</span></span>
<span data-ttu-id="b5561-109">**New-AzServiceBusKey** cmdlet 'i belirtilen ad alanı veya sıra veya konu ve yetkilendirme kuralı için yeni birincil veya ikincil bağlantı dizeleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="b5561-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5561-110">EXAMPLES</span></span>

### <span data-ttu-id="b5561-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5561-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="b5561-112">Ad alanı için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="b5561-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b5561-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="b5561-114">Ad alanı için sağlanan anahtar değerini içeren birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="b5561-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b5561-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="b5561-116">Sıranın birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="b5561-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="b5561-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="b5561-118">Sıra için sağlanan anahtar değerini içeren birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="b5561-119">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="b5561-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="b5561-120">Konu için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="b5561-121">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="b5561-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="b5561-122">Konu için sağlanan anahtar değeri ile birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5561-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="b5561-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5561-123">PARAMETERS</span></span>

### <span data-ttu-id="b5561-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5561-124">-DefaultProfile</span></span>
<span data-ttu-id="b5561-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5561-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5561-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="b5561-126">-KeyValue</span></span>
<span data-ttu-id="b5561-127">SAS belirtecini imzalamak ve doğrulamak için Base64 ile kodlanmış 256 bit anahtar.</span><span class="sxs-lookup"><span data-stu-id="b5561-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5561-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5561-128">-Name</span></span>
<span data-ttu-id="b5561-129">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="b5561-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b5561-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b5561-130">-Namespace</span></span>
<span data-ttu-id="b5561-131">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b5561-131">Namespace Name</span></span>

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

### <span data-ttu-id="b5561-132">-Sıra</span><span class="sxs-lookup"><span data-stu-id="b5561-132">-Queue</span></span>
<span data-ttu-id="b5561-133">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="b5561-133">Queue Name</span></span>

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

### <span data-ttu-id="b5561-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="b5561-134">-RegenerateKey</span></span>
<span data-ttu-id="b5561-135">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="b5561-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5561-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5561-136">-ResourceGroupName</span></span>
<span data-ttu-id="b5561-137">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b5561-137">Resource Group Name</span></span>

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

### <span data-ttu-id="b5561-138">-Konu</span><span class="sxs-lookup"><span data-stu-id="b5561-138">-Topic</span></span>
<span data-ttu-id="b5561-139">Konu adı</span><span class="sxs-lookup"><span data-stu-id="b5561-139">Topic Name</span></span>

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

### <span data-ttu-id="b5561-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5561-140">-Confirm</span></span>
<span data-ttu-id="b5561-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5561-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5561-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5561-142">-WhatIf</span></span>
<span data-ttu-id="b5561-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5561-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5561-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5561-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5561-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5561-145">CommonParameters</span></span>
<span data-ttu-id="b5561-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5561-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5561-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5561-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5561-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5561-148">INPUTS</span></span>

### <span data-ttu-id="b5561-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b5561-149">System.String</span></span>

## <span data-ttu-id="b5561-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5561-150">OUTPUTS</span></span>

### <span data-ttu-id="b5561-151">Microsoft. Azure. Commands. ServiceBus. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b5561-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="b5561-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5561-152">NOTES</span></span>

## <span data-ttu-id="b5561-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5561-153">RELATED LINKS</span></span>
