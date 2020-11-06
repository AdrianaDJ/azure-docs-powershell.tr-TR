---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 6efd58497adc1e59f1bf6d2c2151386ee773f66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592731"
---
# <span data-ttu-id="04a72-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="04a72-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="04a72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a72-102">SYNOPSIS</span></span>
<span data-ttu-id="04a72-103">Hizmet veri yolu ad alanı veya sıra veya konu için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04a72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04a72-104">SYNTAX</span></span>

### <span data-ttu-id="04a72-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04a72-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04a72-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="04a72-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04a72-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="04a72-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04a72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="04a72-108">DESCRIPTION</span></span>
<span data-ttu-id="04a72-109">**Yeni-AzureRmServiceBusKey** cmdlet 'i belirtilen ad alanı veya sıra veya konu ve yetkilendirme kuralı için yeni birincil veya ikincil bağlantı dizeleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="04a72-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04a72-110">EXAMPLES</span></span>

### <span data-ttu-id="04a72-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04a72-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="04a72-112">Ad alanı için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="04a72-113">Örnek 1,1</span><span class="sxs-lookup"><span data-stu-id="04a72-113">Example 1.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="04a72-114">Ad alanı için sağlanan anahtar değerini içeren birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="04a72-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="04a72-115">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="04a72-116">Sıranın birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="04a72-117">Örnek 2,2</span><span class="sxs-lookup"><span data-stu-id="04a72-117">Example 2.2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="04a72-118">Sıra için sağlanan anahtar değerini içeren birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="04a72-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="04a72-119">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="04a72-120">Konu için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="04a72-121">Örnek 3,1</span><span class="sxs-lookup"><span data-stu-id="04a72-121">Example 3.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="04a72-122">Konu için sağlanan anahtar değeri ile birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a72-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="04a72-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04a72-123">PARAMETERS</span></span>

### <span data-ttu-id="04a72-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a72-124">-DefaultProfile</span></span>
<span data-ttu-id="04a72-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04a72-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04a72-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="04a72-126">-KeyValue</span></span>
<span data-ttu-id="04a72-127">SAS belirtecini imzalamak ve doğrulamak için Base64 ile kodlanmış 256 bit anahtar.</span><span class="sxs-lookup"><span data-stu-id="04a72-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="04a72-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="04a72-128">-Name</span></span>
<span data-ttu-id="04a72-129">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="04a72-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="04a72-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="04a72-130">-Namespace</span></span>
<span data-ttu-id="04a72-131">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="04a72-131">Namespace Name</span></span>

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

### <span data-ttu-id="04a72-132">-Sıra</span><span class="sxs-lookup"><span data-stu-id="04a72-132">-Queue</span></span>
<span data-ttu-id="04a72-133">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="04a72-133">Queue Name</span></span>

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

### <span data-ttu-id="04a72-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="04a72-134">-RegenerateKey</span></span>
<span data-ttu-id="04a72-135">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="04a72-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="04a72-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a72-136">-ResourceGroupName</span></span>
<span data-ttu-id="04a72-137">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="04a72-137">Resource Group Name</span></span>

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

### <span data-ttu-id="04a72-138">-Konu</span><span class="sxs-lookup"><span data-stu-id="04a72-138">-Topic</span></span>
<span data-ttu-id="04a72-139">Konu adı</span><span class="sxs-lookup"><span data-stu-id="04a72-139">Topic Name</span></span>

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

### <span data-ttu-id="04a72-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="04a72-140">-Confirm</span></span>
<span data-ttu-id="04a72-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04a72-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a72-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a72-142">-WhatIf</span></span>
<span data-ttu-id="04a72-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04a72-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a72-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04a72-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a72-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a72-145">CommonParameters</span></span>
<span data-ttu-id="04a72-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04a72-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a72-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a72-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a72-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04a72-148">INPUTS</span></span>

### <span data-ttu-id="04a72-149">System. String</span><span class="sxs-lookup"><span data-stu-id="04a72-149">System.String</span></span>

## <span data-ttu-id="04a72-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04a72-150">OUTPUTS</span></span>

### <span data-ttu-id="04a72-151">Microsoft. Azure. Commands. ServiceBus. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="04a72-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="04a72-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04a72-152">NOTES</span></span>

## <span data-ttu-id="04a72-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04a72-153">RELATED LINKS</span></span>
