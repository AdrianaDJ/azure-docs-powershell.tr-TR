---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275460"
---
# <span data-ttu-id="4c60b-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="4c60b-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="4c60b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c60b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c60b-103">Belirtilen olay hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c60b-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="4c60b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c60b-104">SYNTAX</span></span>

### <span data-ttu-id="4c60b-105">EventhubDefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c60b-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c60b-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c60b-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c60b-107">Eventhubresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4c60b-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c60b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c60b-108">DESCRIPTION</span></span>
<span data-ttu-id="4c60b-109">Remove-AzEventHub cmdlet, verilen ad alanından belirtilen olay hub 'ını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="4c60b-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="4c60b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c60b-110">EXAMPLES</span></span>

### <span data-ttu-id="4c60b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4c60b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="4c60b-112">Olay Hub \` myeventhubname 'i kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="4c60b-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="4c60b-113">Örnek 2: InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="4c60b-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="4c60b-114">Örnek 3: boru kullanarak InputObject:</span><span class="sxs-lookup"><span data-stu-id="4c60b-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="4c60b-115">Örnek 4: RESOURCEID-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="4c60b-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="4c60b-116">Örnek 5: RESOURCEID-dize kullanarak:</span><span class="sxs-lookup"><span data-stu-id="4c60b-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="4c60b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c60b-117">PARAMETERS</span></span>

### <span data-ttu-id="4c60b-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="4c60b-118">-AsJob</span></span>
<span data-ttu-id="4c60b-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4c60b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c60b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c60b-120">-DefaultProfile</span></span>
<span data-ttu-id="4c60b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c60b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c60b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c60b-122">-InputObject</span></span>
<span data-ttu-id="4c60b-123">Eventhub nesnesi</span><span class="sxs-lookup"><span data-stu-id="4c60b-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c60b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c60b-124">-Name</span></span>
<span data-ttu-id="4c60b-125">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="4c60b-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c60b-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4c60b-126">-Namespace</span></span>
<span data-ttu-id="4c60b-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="4c60b-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c60b-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4c60b-128">-PassThru</span></span>
<span data-ttu-id="4c60b-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="4c60b-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4c60b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c60b-130">-ResourceGroupName</span></span>
<span data-ttu-id="4c60b-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4c60b-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c60b-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4c60b-132">-ResourceId</span></span>
<span data-ttu-id="4c60b-133">Eventhub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4c60b-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c60b-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c60b-134">-Confirm</span></span>
<span data-ttu-id="4c60b-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c60b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c60b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c60b-136">-WhatIf</span></span>
<span data-ttu-id="4c60b-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c60b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c60b-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c60b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c60b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c60b-139">CommonParameters</span></span>
<span data-ttu-id="4c60b-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c60b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c60b-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c60b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c60b-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c60b-142">INPUTS</span></span>

### <span data-ttu-id="4c60b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4c60b-143">System.String</span></span>

### <span data-ttu-id="4c60b-144">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="4c60b-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="4c60b-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c60b-145">OUTPUTS</span></span>

### <span data-ttu-id="4c60b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c60b-146">System.Boolean</span></span>

## <span data-ttu-id="4c60b-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c60b-147">NOTES</span></span>

## <span data-ttu-id="4c60b-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c60b-148">RELATED LINKS</span></span>
