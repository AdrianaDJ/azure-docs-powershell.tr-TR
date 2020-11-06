---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: 31ed4d8765599fcc99f58870b347a14cdaf00162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591955"
---
# <span data-ttu-id="c467a-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="c467a-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="c467a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c467a-102">SYNOPSIS</span></span>
<span data-ttu-id="c467a-103">Belirtilen olay hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c467a-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c467a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c467a-104">SYNTAX</span></span>

### <span data-ttu-id="c467a-105">EventhubDefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c467a-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c467a-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c467a-106">EventhubInputObjectSet</span></span>
```
Remove-AzureRmEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c467a-107">Eventhubresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c467a-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c467a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c467a-108">DESCRIPTION</span></span>
<span data-ttu-id="c467a-109">Remove-AzureRmEventHub cmdlet, verilen ad alanından belirtilen olay hub 'ını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="c467a-109">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="c467a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c467a-110">EXAMPLES</span></span>

### <span data-ttu-id="c467a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c467a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="c467a-112">Olay Hub \` myeventhubname 'i kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="c467a-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="c467a-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="c467a-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -InputObject $inputobject
```

### <span data-ttu-id="c467a-114">Örnek 2,2-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="c467a-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHub <params> | Remove-AzureRmEventHub
```

### <span data-ttu-id="c467a-115">Örnek 3,1-RESOURCEID-değişken kullanarak:</span><span class="sxs-lookup"><span data-stu-id="c467a-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="c467a-116">Örnek 3,1-RESOURCEID-dize kullanarak:</span><span class="sxs-lookup"><span data-stu-id="c467a-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="c467a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c467a-117">PARAMETERS</span></span>

### <span data-ttu-id="c467a-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="c467a-118">-AsJob</span></span>
<span data-ttu-id="c467a-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c467a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c467a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c467a-120">-DefaultProfile</span></span>
<span data-ttu-id="c467a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c467a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c467a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c467a-122">-InputObject</span></span>
<span data-ttu-id="c467a-123">Eventhub nesnesi</span><span class="sxs-lookup"><span data-stu-id="c467a-123">Eventhub Object</span></span>

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

### <span data-ttu-id="c467a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="c467a-124">-Name</span></span>
<span data-ttu-id="c467a-125">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="c467a-125">EventHub Name</span></span>

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

### <span data-ttu-id="c467a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c467a-126">-Namespace</span></span>
<span data-ttu-id="c467a-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="c467a-127">Namespace Name</span></span>

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

### <span data-ttu-id="c467a-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c467a-128">-PassThru</span></span>
<span data-ttu-id="c467a-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="c467a-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c467a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c467a-130">-ResourceGroupName</span></span>
<span data-ttu-id="c467a-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c467a-131">Resource Group Name</span></span>

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

### <span data-ttu-id="c467a-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c467a-132">-ResourceId</span></span>
<span data-ttu-id="c467a-133">Eventhub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c467a-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="c467a-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="c467a-134">-Confirm</span></span>
<span data-ttu-id="c467a-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c467a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c467a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c467a-136">-WhatIf</span></span>
<span data-ttu-id="c467a-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c467a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c467a-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c467a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c467a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c467a-139">CommonParameters</span></span>
<span data-ttu-id="c467a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c467a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c467a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c467a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c467a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c467a-142">INPUTS</span></span>

### <span data-ttu-id="c467a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c467a-143">System.String</span></span>

### <span data-ttu-id="c467a-144">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="c467a-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>
<span data-ttu-id="c467a-145">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c467a-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c467a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c467a-146">OUTPUTS</span></span>

### <span data-ttu-id="c467a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c467a-147">System.Boolean</span></span>

## <span data-ttu-id="c467a-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c467a-148">NOTES</span></span>

## <span data-ttu-id="c467a-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c467a-149">RELATED LINKS</span></span>
