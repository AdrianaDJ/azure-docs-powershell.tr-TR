---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 1e53e1a1eb1070a9f13c9e67ea4a838358012a13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751949"
---
# <span data-ttu-id="73c7f-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="73c7f-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="73c7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="73c7f-103">Belirtilen olay hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73c7f-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="73c7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73c7f-104">SYNTAX</span></span>

### <span data-ttu-id="73c7f-105">EventhubDefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73c7f-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c7f-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="73c7f-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c7f-107">Eventhubresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="73c7f-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c7f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="73c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="73c7f-109">Remove-AzEventHub cmdlet, verilen ad alanından belirtilen olay hub 'ını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="73c7f-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="73c7f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73c7f-110">EXAMPLES</span></span>

### <span data-ttu-id="73c7f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="73c7f-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="73c7f-112">Olay Hub \` myeventhubname 'i kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="73c7f-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="73c7f-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="73c7f-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="73c7f-114">Örnek 2,2-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="73c7f-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="73c7f-115">Örnek 3,1-RESOURCEID-değişken kullanarak:</span><span class="sxs-lookup"><span data-stu-id="73c7f-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="73c7f-116">Örnek 3,1-RESOURCEID-dize kullanarak:</span><span class="sxs-lookup"><span data-stu-id="73c7f-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="73c7f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73c7f-117">PARAMETERS</span></span>

### <span data-ttu-id="73c7f-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="73c7f-118">-AsJob</span></span>
<span data-ttu-id="73c7f-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="73c7f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73c7f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c7f-120">-DefaultProfile</span></span>
<span data-ttu-id="73c7f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73c7f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73c7f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73c7f-122">-InputObject</span></span>
<span data-ttu-id="73c7f-123">Eventhub nesnesi</span><span class="sxs-lookup"><span data-stu-id="73c7f-123">Eventhub Object</span></span>

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

### <span data-ttu-id="73c7f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="73c7f-124">-Name</span></span>
<span data-ttu-id="73c7f-125">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="73c7f-125">EventHub Name</span></span>

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

### <span data-ttu-id="73c7f-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73c7f-126">-Namespace</span></span>
<span data-ttu-id="73c7f-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="73c7f-127">Namespace Name</span></span>

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

### <span data-ttu-id="73c7f-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="73c7f-128">-PassThru</span></span>
<span data-ttu-id="73c7f-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="73c7f-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="73c7f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c7f-130">-ResourceGroupName</span></span>
<span data-ttu-id="73c7f-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="73c7f-131">Resource Group Name</span></span>

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

### <span data-ttu-id="73c7f-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="73c7f-132">-ResourceId</span></span>
<span data-ttu-id="73c7f-133">Eventhub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="73c7f-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="73c7f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="73c7f-134">-Confirm</span></span>
<span data-ttu-id="73c7f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73c7f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c7f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c7f-136">-WhatIf</span></span>
<span data-ttu-id="73c7f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73c7f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c7f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73c7f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c7f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c7f-139">CommonParameters</span></span>
<span data-ttu-id="73c7f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73c7f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c7f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c7f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c7f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73c7f-142">INPUTS</span></span>

### <span data-ttu-id="73c7f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="73c7f-143">System.String</span></span>

### <span data-ttu-id="73c7f-144">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="73c7f-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="73c7f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73c7f-145">OUTPUTS</span></span>

### <span data-ttu-id="73c7f-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73c7f-146">System.Boolean</span></span>

## <span data-ttu-id="73c7f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73c7f-147">NOTES</span></span>

## <span data-ttu-id="73c7f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73c7f-148">RELATED LINKS</span></span>
