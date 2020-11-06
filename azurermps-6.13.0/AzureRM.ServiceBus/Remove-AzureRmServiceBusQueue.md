---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: ba59f19183cf49802240d7631b99b3e69a9bc6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590864"
---
# <span data-ttu-id="7b123-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="7b123-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="7b123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b123-102">SYNOPSIS</span></span>
<span data-ttu-id="7b123-103">Sırayı belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7b123-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b123-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b123-104">SYNTAX</span></span>

### <span data-ttu-id="7b123-105">QueuePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7b123-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b123-106">Queueınputobjectset</span><span class="sxs-lookup"><span data-stu-id="7b123-106">QueueInputObjectSet</span></span>
```
Remove-AzureRmServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b123-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7b123-107">QueueResourceIdSet</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b123-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b123-108">DESCRIPTION</span></span>
<span data-ttu-id="7b123-109">**Remove-AzureRmServiceBusQueue** cmdlet 'i, sırayı belirtilen hizmet veri yolu ad alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7b123-109">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7b123-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b123-110">EXAMPLES</span></span>

### <span data-ttu-id="7b123-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7b123-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="7b123-112">Hizmet veri yolu kuyruğunu `SB-Queue_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7b123-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="7b123-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="7b123-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="7b123-114">$İnputobject for-InputObject parametresinde sağlanan hizmet veri yolu kuyruğunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="7b123-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="7b123-115">Örnek 2,1-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="7b123-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzureRmServiceBusQueue <params> | Remove-AzureRmServiceBusQueue
```

### <span data-ttu-id="7b123-116">Örnek 3,1-RESOURCEID-değişken kullanarak:</span><span class="sxs-lookup"><span data-stu-id="7b123-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="7b123-117">$Resourceid/String for-RESOURCEID parametresindeki ARM kimliğinde sağlanan hizmet veri yolu kuyruğunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="7b123-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="7b123-118">Örnek 3,2-RESOURCEID-passign as dizesi:</span><span class="sxs-lookup"><span data-stu-id="7b123-118">Example 3.2 - ResourceId - passign as string:</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="7b123-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b123-119">PARAMETERS</span></span>

### <span data-ttu-id="7b123-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="7b123-120">-AsJob</span></span>
<span data-ttu-id="7b123-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7b123-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b123-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b123-122">-DefaultProfile</span></span>
<span data-ttu-id="7b123-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b123-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b123-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b123-124">-InputObject</span></span>
<span data-ttu-id="7b123-125">Hizmet veri yolu sıra nesnesi</span><span class="sxs-lookup"><span data-stu-id="7b123-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="7b123-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="7b123-126">-Name</span></span>
<span data-ttu-id="7b123-127">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="7b123-127">Queue Name</span></span>

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

### <span data-ttu-id="7b123-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7b123-128">-Namespace</span></span>
<span data-ttu-id="7b123-129">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="7b123-129">Namespace Name</span></span>

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

### <span data-ttu-id="7b123-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7b123-130">-PassThru</span></span>
<span data-ttu-id="7b123-131">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="7b123-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7b123-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b123-132">-ResourceGroupName</span></span>
<span data-ttu-id="7b123-133">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7b123-133">The name of the resource group</span></span>

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

### <span data-ttu-id="7b123-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7b123-134">-ResourceId</span></span>
<span data-ttu-id="7b123-135">Hizmet veri yolu kuyruğu kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7b123-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="7b123-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b123-136">-Confirm</span></span>
<span data-ttu-id="7b123-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b123-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b123-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b123-138">-WhatIf</span></span>
<span data-ttu-id="7b123-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b123-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b123-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b123-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b123-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b123-141">CommonParameters</span></span>
<span data-ttu-id="7b123-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b123-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b123-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b123-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b123-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b123-144">INPUTS</span></span>

### <span data-ttu-id="7b123-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7b123-145">System.String</span></span>

### <span data-ttu-id="7b123-146">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="7b123-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>
<span data-ttu-id="7b123-147">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b123-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7b123-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b123-148">OUTPUTS</span></span>

### <span data-ttu-id="7b123-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b123-149">System.Boolean</span></span>

## <span data-ttu-id="7b123-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b123-150">NOTES</span></span>

## <span data-ttu-id="7b123-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b123-151">RELATED LINKS</span></span>
