---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: 23aff5b896664321033183ad35909300f9a5c3b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932458"
---
# <span data-ttu-id="6e63c-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6e63c-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="6e63c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e63c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e63c-103">Sırayı belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e63c-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6e63c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e63c-104">SYNTAX</span></span>

### <span data-ttu-id="6e63c-105">QueuePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e63c-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e63c-106">Queueınputobjectset</span><span class="sxs-lookup"><span data-stu-id="6e63c-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e63c-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6e63c-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e63c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e63c-108">DESCRIPTION</span></span>
<span data-ttu-id="6e63c-109">**Remove-AzServiceBusQueue** cmdlet 'i, sırayı belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e63c-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6e63c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e63c-110">EXAMPLES</span></span>

### <span data-ttu-id="6e63c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6e63c-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="6e63c-112">Hizmet veri yolu kuyruğunu `SB-Queue_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="6e63c-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="6e63c-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="6e63c-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="6e63c-114">$İnputobject for-InputObject parametresinde sağlanan hizmet veri yolu kuyruğunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="6e63c-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="6e63c-115">Örnek 2,1-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="6e63c-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="6e63c-116">Örnek 3,1-RESOURCEID-değişken kullanarak:</span><span class="sxs-lookup"><span data-stu-id="6e63c-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="6e63c-117">$Resourceid/String for-RESOURCEID parametresindeki ARM kimliğinde sağlanan hizmet veri yolu kuyruğunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="6e63c-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="6e63c-118">Örnek 3,2-RESOURCEID-dize olarak geçiliyor:</span><span class="sxs-lookup"><span data-stu-id="6e63c-118">Example 3.2 - ResourceId - passing as string:</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="6e63c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e63c-119">PARAMETERS</span></span>

### <span data-ttu-id="6e63c-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="6e63c-120">-AsJob</span></span>
<span data-ttu-id="6e63c-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6e63c-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e63c-122">-DefaultProfile</span></span>
<span data-ttu-id="6e63c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e63c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e63c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e63c-124">-InputObject</span></span>
<span data-ttu-id="6e63c-125">Hizmet veri yolu sıra nesnesi</span><span class="sxs-lookup"><span data-stu-id="6e63c-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e63c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e63c-126">-Name</span></span>
<span data-ttu-id="6e63c-127">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="6e63c-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e63c-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e63c-128">-Namespace</span></span>
<span data-ttu-id="6e63c-129">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="6e63c-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e63c-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6e63c-130">-PassThru</span></span>
<span data-ttu-id="6e63c-131">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="6e63c-131">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e63c-132">-ResourceGroupName</span></span>
<span data-ttu-id="6e63c-133">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6e63c-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e63c-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6e63c-134">-ResourceId</span></span>
<span data-ttu-id="6e63c-135">Hizmet veri yolu kuyruğu kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6e63c-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e63c-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e63c-136">-Confirm</span></span>
<span data-ttu-id="6e63c-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e63c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e63c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e63c-138">-WhatIf</span></span>
<span data-ttu-id="6e63c-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e63c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e63c-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e63c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e63c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e63c-141">CommonParameters</span></span>
<span data-ttu-id="6e63c-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e63c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e63c-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e63c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e63c-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e63c-144">INPUTS</span></span>

### <span data-ttu-id="6e63c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6e63c-145">System.String</span></span>

### <span data-ttu-id="6e63c-146">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="6e63c-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="6e63c-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e63c-147">OUTPUTS</span></span>

### <span data-ttu-id="6e63c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e63c-148">System.Boolean</span></span>

## <span data-ttu-id="6e63c-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e63c-149">NOTES</span></span>

## <span data-ttu-id="6e63c-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e63c-150">RELATED LINKS</span></span>