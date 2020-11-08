---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279614"
---
# <span data-ttu-id="1dd32-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="1dd32-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="1dd32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd32-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd32-103">Belirtilen hizmet veri yolu ad boşluğundan konuyu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1dd32-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1dd32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dd32-104">SYNTAX</span></span>

### <span data-ttu-id="1dd32-105">Topıcpropertiesset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1dd32-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd32-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1dd32-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd32-107">Topicresourceıdset</span><span class="sxs-lookup"><span data-stu-id="1dd32-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd32-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dd32-108">DESCRIPTION</span></span>
<span data-ttu-id="1dd32-109">**Remove-AzServiceBusTopic** cmdlet 'i, konuyu belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1dd32-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1dd32-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dd32-110">EXAMPLES</span></span>

### <span data-ttu-id="1dd32-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1dd32-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="1dd32-112">Başlığı `SB-Topic_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="1dd32-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="1dd32-113">Örnek 2: InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="1dd32-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="1dd32-114">Örnek 3: InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="1dd32-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="1dd32-115">Örnek 4: değişken kullanan RESOURCEID:</span><span class="sxs-lookup"><span data-stu-id="1dd32-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="1dd32-116">Örnek 5: dize değeri kullanan RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1dd32-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="1dd32-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dd32-117">PARAMETERS</span></span>

### <span data-ttu-id="1dd32-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="1dd32-118">-AsJob</span></span>
<span data-ttu-id="1dd32-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1dd32-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dd32-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd32-120">-DefaultProfile</span></span>
<span data-ttu-id="1dd32-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dd32-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd32-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dd32-122">-InputObject</span></span>
<span data-ttu-id="1dd32-123">Hizmet veri yolu konu nesnesi</span><span class="sxs-lookup"><span data-stu-id="1dd32-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="1dd32-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dd32-124">-Name</span></span>
<span data-ttu-id="1dd32-125">Konu adı</span><span class="sxs-lookup"><span data-stu-id="1dd32-125">Topic Name</span></span>

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

### <span data-ttu-id="1dd32-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1dd32-126">-Namespace</span></span>
<span data-ttu-id="1dd32-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="1dd32-127">Namespace Name</span></span>

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

### <span data-ttu-id="1dd32-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1dd32-128">-PassThru</span></span>
<span data-ttu-id="1dd32-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="1dd32-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1dd32-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd32-130">-ResourceGroupName</span></span>
<span data-ttu-id="1dd32-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="1dd32-131">The name of the resource group</span></span>

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

### <span data-ttu-id="1dd32-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1dd32-132">-ResourceId</span></span>
<span data-ttu-id="1dd32-133">Hizmet veri yolu başlığı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1dd32-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="1dd32-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1dd32-134">-Confirm</span></span>
<span data-ttu-id="1dd32-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1dd32-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd32-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd32-136">-WhatIf</span></span>
<span data-ttu-id="1dd32-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1dd32-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd32-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1dd32-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd32-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd32-139">CommonParameters</span></span>
<span data-ttu-id="1dd32-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dd32-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd32-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd32-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd32-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dd32-142">INPUTS</span></span>

### <span data-ttu-id="1dd32-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd32-143">System.String</span></span>

### <span data-ttu-id="1dd32-144">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="1dd32-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="1dd32-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dd32-145">OUTPUTS</span></span>

### <span data-ttu-id="1dd32-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dd32-146">System.Boolean</span></span>

## <span data-ttu-id="1dd32-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dd32-147">NOTES</span></span>

## <span data-ttu-id="1dd32-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dd32-148">RELATED LINKS</span></span>
