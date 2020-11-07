---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764772"
---
# <span data-ttu-id="edc26-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="edc26-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="edc26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edc26-102">SYNOPSIS</span></span>
<span data-ttu-id="edc26-103">Hizmet veri yolu sırasının birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edc26-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edc26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edc26-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edc26-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edc26-105">DESCRIPTION</span></span>
<span data-ttu-id="edc26-106">**Yeni-AzureRmServiceBusQueueKey** cmdlet 'ı belirtilen hizmet veri yolu kuyruğu ve yetkilendirme kuralı için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edc26-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="edc26-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edc26-107">EXAMPLES</span></span>

### <span data-ttu-id="edc26-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="edc26-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="edc26-109">Ad alanı için birincil bağlantı dizesini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edc26-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="edc26-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="edc26-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="edc26-111">Ad alanı için ikincil bağlantı dizesini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edc26-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="edc26-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edc26-112">PARAMETERS</span></span>

### <span data-ttu-id="edc26-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="edc26-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="edc26-114">Yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="edc26-114">The authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc26-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="edc26-115">-NamespaceName</span></span>
<span data-ttu-id="edc26-116">Hizmet veri yolu ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="edc26-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc26-117">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="edc26-117">-QueueName</span></span>
<span data-ttu-id="edc26-118">Hizmet veri yolu sıra adı.</span><span class="sxs-lookup"><span data-stu-id="edc26-118">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc26-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="edc26-119">-RegenerateKeys</span></span>
<span data-ttu-id="edc26-120">Birincil veya ikincil anahtarların yeniden oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edc26-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc26-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="edc26-121">-ResourceGroup</span></span>
<span data-ttu-id="edc26-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="edc26-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc26-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="edc26-123">-Confirm</span></span>
<span data-ttu-id="edc26-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edc26-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc26-125">-WhatIf</span></span>
<span data-ttu-id="edc26-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edc26-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edc26-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edc26-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc26-128">CommonParameters</span></span>
<span data-ttu-id="edc26-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edc26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc26-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc26-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc26-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edc26-131">INPUTS</span></span>

### <span data-ttu-id="edc26-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="edc26-132">-ResourceGroup</span></span>
 <span data-ttu-id="edc26-133">System. String</span><span class="sxs-lookup"><span data-stu-id="edc26-133">System.String</span></span>
 

### <span data-ttu-id="edc26-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="edc26-134">-NamespaceName</span></span>
 <span data-ttu-id="edc26-135">System. String</span><span class="sxs-lookup"><span data-stu-id="edc26-135">System.String</span></span>
 

### <span data-ttu-id="edc26-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="edc26-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="edc26-137">System. String</span><span class="sxs-lookup"><span data-stu-id="edc26-137">System.String</span></span>
 

### <span data-ttu-id="edc26-138">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="edc26-138">-QueueName</span></span>
 <span data-ttu-id="edc26-139">System. String</span><span class="sxs-lookup"><span data-stu-id="edc26-139">System.String</span></span>
 

### <span data-ttu-id="edc26-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="edc26-140">-RegenerateKeys</span></span>
 <span data-ttu-id="edc26-141">System. String</span><span class="sxs-lookup"><span data-stu-id="edc26-141">System.String</span></span>

## <span data-ttu-id="edc26-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edc26-142">OUTPUTS</span></span>

### <span data-ttu-id="edc26-143">Microsoft. Azure. Management. ServiceBus. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="edc26-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="edc26-144">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {PrimaryKey değeri} SecondaryKey: {SecondaryKey Value} AnahtarAdı: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="edc26-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="edc26-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edc26-145">NOTES</span></span>

## <span data-ttu-id="edc26-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edc26-146">RELATED LINKS</span></span>

