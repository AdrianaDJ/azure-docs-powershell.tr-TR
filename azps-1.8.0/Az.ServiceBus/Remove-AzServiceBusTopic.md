---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 27d35f0c5b0e947624827d01d1182a09912cb9fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759155"
---
# <span data-ttu-id="124cd-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="124cd-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="124cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="124cd-102">SYNOPSIS</span></span>
<span data-ttu-id="124cd-103">Belirtilen hizmet veri yolu ad boşluğundan konuyu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="124cd-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="124cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="124cd-104">SYNTAX</span></span>

### <span data-ttu-id="124cd-105">Topıcpropertiesset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="124cd-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="124cd-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="124cd-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="124cd-107">Topicresourceıdset</span><span class="sxs-lookup"><span data-stu-id="124cd-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="124cd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="124cd-108">DESCRIPTION</span></span>
<span data-ttu-id="124cd-109">**Remove-AzServiceBusTopic** cmdlet 'i, konuyu belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="124cd-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="124cd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="124cd-110">EXAMPLES</span></span>

### <span data-ttu-id="124cd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="124cd-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="124cd-112">Başlığı `SB-Topic_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="124cd-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="124cd-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="124cd-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="124cd-114">Örnek 2,2-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="124cd-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="124cd-115">Örnek 3,1-değişken kullanan RESOURCEID:</span><span class="sxs-lookup"><span data-stu-id="124cd-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="124cd-116">Örnek 3,2-dize değeri kullanma</span><span class="sxs-lookup"><span data-stu-id="124cd-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="124cd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="124cd-117">PARAMETERS</span></span>

### <span data-ttu-id="124cd-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="124cd-118">-AsJob</span></span>
<span data-ttu-id="124cd-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="124cd-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="124cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="124cd-120">-DefaultProfile</span></span>
<span data-ttu-id="124cd-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="124cd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="124cd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="124cd-122">-InputObject</span></span>
<span data-ttu-id="124cd-123">Hizmet veri yolu konu nesnesi</span><span class="sxs-lookup"><span data-stu-id="124cd-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="124cd-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="124cd-124">-Name</span></span>
<span data-ttu-id="124cd-125">Konu adı</span><span class="sxs-lookup"><span data-stu-id="124cd-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124cd-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="124cd-126">-Namespace</span></span>
<span data-ttu-id="124cd-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="124cd-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124cd-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="124cd-128">-PassThru</span></span>
<span data-ttu-id="124cd-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="124cd-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="124cd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="124cd-130">-ResourceGroupName</span></span>
<span data-ttu-id="124cd-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="124cd-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124cd-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="124cd-132">-ResourceId</span></span>
<span data-ttu-id="124cd-133">Hizmet veri yolu başlığı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="124cd-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124cd-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="124cd-134">-Confirm</span></span>
<span data-ttu-id="124cd-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="124cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="124cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="124cd-136">-WhatIf</span></span>
<span data-ttu-id="124cd-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="124cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="124cd-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="124cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="124cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124cd-139">CommonParameters</span></span>
<span data-ttu-id="124cd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="124cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124cd-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="124cd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124cd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="124cd-142">INPUTS</span></span>

### <span data-ttu-id="124cd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="124cd-143">System.String</span></span>

### <span data-ttu-id="124cd-144">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="124cd-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="124cd-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="124cd-145">OUTPUTS</span></span>

### <span data-ttu-id="124cd-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="124cd-146">System.Boolean</span></span>

## <span data-ttu-id="124cd-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="124cd-147">NOTES</span></span>

## <span data-ttu-id="124cd-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="124cd-148">RELATED LINKS</span></span>
