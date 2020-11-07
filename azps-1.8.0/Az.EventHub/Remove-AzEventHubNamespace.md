---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 4d5ddbc4dff2922b90bc6d1117ff32473afd9042
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760828"
---
# <span data-ttu-id="5e474-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5e474-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="5e474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e474-102">SYNOPSIS</span></span>
<span data-ttu-id="5e474-103">Belirtilen olay hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e474-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="5e474-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e474-104">SYNTAX</span></span>

### <span data-ttu-id="5e474-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e474-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e474-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e474-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e474-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e474-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e474-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e474-108">DESCRIPTION</span></span>
<span data-ttu-id="5e474-109">Remove-AzEventHubNamespace cmdlet 'i, belirtilen olay hub ad alanını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="5e474-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="5e474-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e474-110">EXAMPLES</span></span>

### <span data-ttu-id="5e474-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e474-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="5e474-112">\` \` Myresourcegroupname kaynak grubundaki Olay Hub ad alanı mynamespacadını kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="5e474-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5e474-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="5e474-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="5e474-114">Örnek 2,1-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="5e474-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="5e474-115">Örnek 3,1-RESOURCEID-değişken kullanma</span><span class="sxs-lookup"><span data-stu-id="5e474-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="5e474-116">Örnek 3,2-RESOURCEID-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="5e474-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="5e474-117">Örnek 3,3-RESOURCEID-dize kullanarak:</span><span class="sxs-lookup"><span data-stu-id="5e474-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="5e474-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e474-118">PARAMETERS</span></span>

### <span data-ttu-id="5e474-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="5e474-119">-AsJob</span></span>
<span data-ttu-id="5e474-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5e474-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e474-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e474-121">-DefaultProfile</span></span>
<span data-ttu-id="5e474-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e474-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e474-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e474-123">-InputObject</span></span>
<span data-ttu-id="5e474-124">EventHubs ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="5e474-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e474-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e474-125">-Name</span></span>
<span data-ttu-id="5e474-126">EventHub ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="5e474-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e474-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5e474-127">-PassThru</span></span>
<span data-ttu-id="5e474-128">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e474-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5e474-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e474-129">-ResourceGroupName</span></span>
<span data-ttu-id="5e474-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5e474-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e474-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5e474-131">-ResourceId</span></span>
<span data-ttu-id="5e474-132">EventHubs ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5e474-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e474-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e474-133">-Confirm</span></span>
<span data-ttu-id="5e474-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e474-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e474-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e474-135">-WhatIf</span></span>
<span data-ttu-id="5e474-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e474-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e474-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e474-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e474-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e474-138">CommonParameters</span></span>
<span data-ttu-id="5e474-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e474-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e474-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e474-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e474-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e474-141">INPUTS</span></span>

### <span data-ttu-id="5e474-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5e474-142">System.String</span></span>

### <span data-ttu-id="5e474-143">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5e474-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5e474-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e474-144">OUTPUTS</span></span>

### <span data-ttu-id="5e474-145">System. void</span><span class="sxs-lookup"><span data-stu-id="5e474-145">System.Void</span></span>

## <span data-ttu-id="5e474-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e474-146">NOTES</span></span>

## <span data-ttu-id="5e474-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e474-147">RELATED LINKS</span></span>
