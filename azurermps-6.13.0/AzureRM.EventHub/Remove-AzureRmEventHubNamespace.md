---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590302"
---
# <span data-ttu-id="a2599-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a2599-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="a2599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2599-102">SYNOPSIS</span></span>
<span data-ttu-id="a2599-103">Belirtilen olay hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2599-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2599-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2599-104">SYNTAX</span></span>

### <span data-ttu-id="a2599-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2599-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2599-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2599-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2599-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2599-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2599-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2599-108">DESCRIPTION</span></span>
<span data-ttu-id="a2599-109">Remove-AzureRmEventHubNamespace cmdlet 'i, belirtilen olay hub ad alanını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="a2599-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a2599-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2599-110">EXAMPLES</span></span>

### <span data-ttu-id="a2599-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a2599-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="a2599-112">\` \` Myresourcegroupname kaynak grubundaki Olay Hub ad alanı mynamespacadını kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="a2599-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a2599-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="a2599-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="a2599-114">Örnek 2,1-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="a2599-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="a2599-115">Örnek 3,1-RESOURCEID-değişken kullanma</span><span class="sxs-lookup"><span data-stu-id="a2599-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="a2599-116">Örnek 3,2-RESOURCEID-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="a2599-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="a2599-117">Örnek 3,3-RESOURCEID-dize kullanarak:</span><span class="sxs-lookup"><span data-stu-id="a2599-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="a2599-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2599-118">PARAMETERS</span></span>

### <span data-ttu-id="a2599-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="a2599-119">-AsJob</span></span>
<span data-ttu-id="a2599-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a2599-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2599-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2599-121">-DefaultProfile</span></span>
<span data-ttu-id="a2599-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2599-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2599-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2599-123">-InputObject</span></span>
<span data-ttu-id="a2599-124">EventHubs ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="a2599-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="a2599-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2599-125">-Name</span></span>
<span data-ttu-id="a2599-126">EventHub ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="a2599-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="a2599-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a2599-127">-PassThru</span></span>
<span data-ttu-id="a2599-128">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="a2599-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a2599-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2599-129">-ResourceGroupName</span></span>
<span data-ttu-id="a2599-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a2599-130">Resource Group Name</span></span>

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

### <span data-ttu-id="a2599-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a2599-131">-ResourceId</span></span>
<span data-ttu-id="a2599-132">EventHubs ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a2599-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="a2599-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2599-133">-Confirm</span></span>
<span data-ttu-id="a2599-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2599-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2599-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2599-135">-WhatIf</span></span>
<span data-ttu-id="a2599-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2599-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2599-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2599-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2599-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2599-138">CommonParameters</span></span>
<span data-ttu-id="a2599-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2599-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2599-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2599-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2599-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2599-141">INPUTS</span></span>

### <span data-ttu-id="a2599-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a2599-142">System.String</span></span>

### <span data-ttu-id="a2599-143">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a2599-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="a2599-144">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2599-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a2599-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2599-145">OUTPUTS</span></span>

### <span data-ttu-id="a2599-146">System. void</span><span class="sxs-lookup"><span data-stu-id="a2599-146">System.Void</span></span>

## <span data-ttu-id="a2599-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2599-147">NOTES</span></span>

## <span data-ttu-id="a2599-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2599-148">RELATED LINKS</span></span>
