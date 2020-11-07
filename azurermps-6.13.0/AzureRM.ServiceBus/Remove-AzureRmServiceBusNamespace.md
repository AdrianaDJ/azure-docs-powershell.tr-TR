---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: c56637b8470e40e6b46984117a764da248684005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762447"
---
# <span data-ttu-id="bf0fc-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bf0fc-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="bf0fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0fc-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf0fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf0fc-104">SYNTAX</span></span>

### <span data-ttu-id="bf0fc-105">NamespacePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf0fc-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0fc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bf0fc-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0fc-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf0fc-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf0fc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf0fc-108">DESCRIPTION</span></span>
<span data-ttu-id="bf0fc-109">**Remove-AzureRmServiceBusNamespace** cmdlet 'i belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-109">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="bf0fc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf0fc-110">EXAMPLES</span></span>

### <span data-ttu-id="bf0fc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf0fc-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="bf0fc-112">Belirtilen kaynak grubundan hizmet veri yolu ad alanını kaldırır `SB-Example1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="bf0fc-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="bf0fc-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="bf0fc-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusNamespace <params>
PS C:\> Remove-AzureRmServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="bf0fc-114">$İnputobject ile sağlanan hizmet veri yolu ad boşluğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="bf0fc-115">Örnek 2,2-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="bf0fc-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace <params> | Remove-AzureRmServiceBusNamespace
```

<span data-ttu-id="bf0fc-116">Yöneltme kullanarak hizmet veri yolu ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="bf0fc-117">Örnek 3-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf0fc-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzureRmResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="bf0fc-118">$Resourceid-RESOURCEID parametresi veya boru üzerinden ARM kimliği aracılığıyla sağlanan hizmet veri yolu ad boşluğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="bf0fc-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf0fc-119">PARAMETERS</span></span>

### <span data-ttu-id="bf0fc-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="bf0fc-120">-AsJob</span></span>
<span data-ttu-id="bf0fc-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bf0fc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf0fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0fc-122">-DefaultProfile</span></span>
<span data-ttu-id="bf0fc-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0fc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf0fc-124">-InputObject</span></span>
<span data-ttu-id="bf0fc-125">Hizmet veri yolu ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="bf0fc-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="bf0fc-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf0fc-126">-Name</span></span>
<span data-ttu-id="bf0fc-127">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-127">Namespace Name.</span></span>

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

### <span data-ttu-id="bf0fc-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bf0fc-128">-PassThru</span></span>
<span data-ttu-id="bf0fc-129">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bf0fc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0fc-130">-ResourceGroupName</span></span>
<span data-ttu-id="bf0fc-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="bf0fc-131">The name of the resource group</span></span>

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

### <span data-ttu-id="bf0fc-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf0fc-132">-ResourceId</span></span>
<span data-ttu-id="bf0fc-133">Hizmet veri yolu ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="bf0fc-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="bf0fc-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf0fc-134">-Confirm</span></span>
<span data-ttu-id="bf0fc-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf0fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0fc-136">-WhatIf</span></span>
<span data-ttu-id="bf0fc-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf0fc-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf0fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0fc-139">CommonParameters</span></span>
<span data-ttu-id="bf0fc-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0fc-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf0fc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0fc-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf0fc-142">INPUTS</span></span>

### <span data-ttu-id="bf0fc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bf0fc-143">System.String</span></span>

### <span data-ttu-id="bf0fc-144">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bf0fc-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="bf0fc-145">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf0fc-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bf0fc-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf0fc-146">OUTPUTS</span></span>

### <span data-ttu-id="bf0fc-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf0fc-147">System.Boolean</span></span>

## <span data-ttu-id="bf0fc-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf0fc-148">NOTES</span></span>

## <span data-ttu-id="bf0fc-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf0fc-149">RELATED LINKS</span></span>
