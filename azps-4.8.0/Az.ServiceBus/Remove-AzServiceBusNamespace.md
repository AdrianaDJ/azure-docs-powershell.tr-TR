---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268804"
---
# <span data-ttu-id="370d4-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="370d4-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="370d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="370d4-102">SYNOPSIS</span></span>
<span data-ttu-id="370d4-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="370d4-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="370d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="370d4-104">SYNTAX</span></span>

### <span data-ttu-id="370d4-105">NamespacePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="370d4-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="370d4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="370d4-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="370d4-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="370d4-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="370d4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="370d4-108">DESCRIPTION</span></span>
<span data-ttu-id="370d4-109">**Remove-AzServiceBusNamespace** cmdlet 'i belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="370d4-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="370d4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="370d4-110">EXAMPLES</span></span>

### <span data-ttu-id="370d4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="370d4-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="370d4-112">Belirtilen kaynak grubundan hizmet veri yolu ad alanını kaldırır `SB-Example1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="370d4-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="370d4-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="370d4-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="370d4-114">$İnputobject ile sağlanan hizmet veri yolu ad boşluğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="370d4-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="370d4-115">Örnek 2,2-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="370d4-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="370d4-116">Yöneltme kullanarak hizmet veri yolu ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="370d4-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="370d4-117">Örnek 3-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="370d4-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="370d4-118">$Resourceid-RESOURCEID parametresi veya boru üzerinden ARM kimliği aracılığıyla sağlanan hizmet veri yolu ad boşluğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="370d4-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="370d4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="370d4-119">PARAMETERS</span></span>

### <span data-ttu-id="370d4-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="370d4-120">-AsJob</span></span>
<span data-ttu-id="370d4-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="370d4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="370d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370d4-122">-DefaultProfile</span></span>
<span data-ttu-id="370d4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="370d4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="370d4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="370d4-124">-InputObject</span></span>
<span data-ttu-id="370d4-125">Hizmet veri yolu ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="370d4-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="370d4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="370d4-126">-Name</span></span>
<span data-ttu-id="370d4-127">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="370d4-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370d4-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="370d4-128">-PassThru</span></span>
<span data-ttu-id="370d4-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="370d4-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="370d4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370d4-130">-ResourceGroupName</span></span>
<span data-ttu-id="370d4-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="370d4-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370d4-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="370d4-132">-ResourceId</span></span>
<span data-ttu-id="370d4-133">Hizmet veri yolu ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="370d4-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="370d4-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="370d4-134">-Confirm</span></span>
<span data-ttu-id="370d4-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="370d4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="370d4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="370d4-136">-WhatIf</span></span>
<span data-ttu-id="370d4-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="370d4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="370d4-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="370d4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="370d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370d4-139">CommonParameters</span></span>
<span data-ttu-id="370d4-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="370d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370d4-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="370d4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370d4-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="370d4-142">INPUTS</span></span>

### <span data-ttu-id="370d4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="370d4-143">System.String</span></span>

### <span data-ttu-id="370d4-144">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="370d4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="370d4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="370d4-145">OUTPUTS</span></span>

### <span data-ttu-id="370d4-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="370d4-146">System.Boolean</span></span>

## <span data-ttu-id="370d4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="370d4-147">NOTES</span></span>

## <span data-ttu-id="370d4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="370d4-148">RELATED LINKS</span></span>
