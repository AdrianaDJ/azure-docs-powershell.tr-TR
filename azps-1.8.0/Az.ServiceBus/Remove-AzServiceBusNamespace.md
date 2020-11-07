---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: b17fa7309274f261c329eaf896519f8bb70d06fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759168"
---
# <span data-ttu-id="3a020-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="3a020-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="3a020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a020-102">SYNOPSIS</span></span>
<span data-ttu-id="3a020-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a020-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="3a020-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a020-104">SYNTAX</span></span>

### <span data-ttu-id="3a020-105">NamespacePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a020-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a020-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a020-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a020-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a020-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a020-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a020-108">DESCRIPTION</span></span>
<span data-ttu-id="3a020-109">**Remove-AzServiceBusNamespace** cmdlet 'i belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a020-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="3a020-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a020-110">EXAMPLES</span></span>

### <span data-ttu-id="3a020-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a020-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="3a020-112">Belirtilen kaynak grubundan hizmet veri yolu ad alanını kaldırır `SB-Example1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="3a020-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="3a020-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="3a020-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="3a020-114">$İnputobject ile sağlanan hizmet veri yolu ad boşluğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a020-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="3a020-115">Örnek 2,2-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="3a020-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="3a020-116">Yöneltme kullanarak hizmet veri yolu ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a020-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="3a020-117">Örnek 3-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a020-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="3a020-118">$Resourceid-RESOURCEID parametresi veya boru üzerinden ARM kimliği aracılığıyla sağlanan hizmet veri yolu ad boşluğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a020-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="3a020-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a020-119">PARAMETERS</span></span>

### <span data-ttu-id="3a020-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="3a020-120">-AsJob</span></span>
<span data-ttu-id="3a020-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3a020-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a020-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a020-122">-DefaultProfile</span></span>
<span data-ttu-id="3a020-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a020-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a020-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a020-124">-InputObject</span></span>
<span data-ttu-id="3a020-125">Hizmet veri yolu ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3a020-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="3a020-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a020-126">-Name</span></span>
<span data-ttu-id="3a020-127">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="3a020-127">Namespace Name.</span></span>

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

### <span data-ttu-id="3a020-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a020-128">-PassThru</span></span>
<span data-ttu-id="3a020-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a020-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3a020-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a020-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a020-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3a020-131">The name of the resource group</span></span>

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

### <span data-ttu-id="3a020-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a020-132">-ResourceId</span></span>
<span data-ttu-id="3a020-133">Hizmet veri yolu ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3a020-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="3a020-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a020-134">-Confirm</span></span>
<span data-ttu-id="3a020-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a020-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a020-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a020-136">-WhatIf</span></span>
<span data-ttu-id="3a020-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a020-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a020-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a020-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a020-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a020-139">CommonParameters</span></span>
<span data-ttu-id="3a020-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a020-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a020-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a020-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a020-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a020-142">INPUTS</span></span>

### <span data-ttu-id="3a020-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3a020-143">System.String</span></span>

### <span data-ttu-id="3a020-144">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3a020-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3a020-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a020-145">OUTPUTS</span></span>

### <span data-ttu-id="3a020-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a020-146">System.Boolean</span></span>

## <span data-ttu-id="3a020-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a020-147">NOTES</span></span>

## <span data-ttu-id="3a020-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a020-148">RELATED LINKS</span></span>
