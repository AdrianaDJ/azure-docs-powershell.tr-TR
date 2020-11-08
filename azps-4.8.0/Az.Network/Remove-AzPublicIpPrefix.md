---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267017"
---
# <span data-ttu-id="c48f5-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c48f5-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="c48f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c48f5-103">Genel IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="c48f5-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="c48f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c48f5-104">SYNTAX</span></span>

### <span data-ttu-id="c48f5-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c48f5-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48f5-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c48f5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48f5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c48f5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c48f5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c48f5-108">DESCRIPTION</span></span>
<span data-ttu-id="c48f5-109">**Remove-Azpublicıpprefix** cmdlet 'i, kendisinden herhangi BIR genel IP adresi olmadığı sürece bir Azure genel IP önekini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c48f5-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="c48f5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c48f5-110">EXAMPLES</span></span>

### <span data-ttu-id="c48f5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c48f5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="c48f5-112">$prefixName $rgName kaynak grubundan ortak IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="c48f5-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="c48f5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c48f5-113">PARAMETERS</span></span>

### <span data-ttu-id="c48f5-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="c48f5-114">-AsJob</span></span>
<span data-ttu-id="c48f5-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c48f5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c48f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48f5-116">-DefaultProfile</span></span>
<span data-ttu-id="c48f5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c48f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48f5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c48f5-118">-Force</span></span>
<span data-ttu-id="c48f5-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c48f5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c48f5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c48f5-120">-InputObject</span></span>
<span data-ttu-id="c48f5-121">Publicıpprefix nesnesi</span><span class="sxs-lookup"><span data-stu-id="c48f5-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c48f5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c48f5-122">-Name</span></span>
<span data-ttu-id="c48f5-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c48f5-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48f5-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c48f5-124">-PassThru</span></span>
<span data-ttu-id="c48f5-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c48f5-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c48f5-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c48f5-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c48f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="c48f5-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c48f5-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48f5-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c48f5-129">-ResourceId</span></span>
<span data-ttu-id="c48f5-130">Kaldırılacak kaynağın RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c48f5-130">The resourceId for the resource to remove</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48f5-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="c48f5-131">-Confirm</span></span>
<span data-ttu-id="c48f5-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c48f5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c48f5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c48f5-133">-WhatIf</span></span>
<span data-ttu-id="c48f5-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c48f5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c48f5-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c48f5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c48f5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48f5-136">CommonParameters</span></span>
<span data-ttu-id="c48f5-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c48f5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48f5-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48f5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48f5-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c48f5-139">INPUTS</span></span>

### <span data-ttu-id="c48f5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c48f5-140">System.String</span></span>

### <span data-ttu-id="c48f5-141">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c48f5-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="c48f5-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c48f5-142">OUTPUTS</span></span>

### <span data-ttu-id="c48f5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c48f5-143">System.Boolean</span></span>

## <span data-ttu-id="c48f5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c48f5-144">NOTES</span></span>

## <span data-ttu-id="c48f5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c48f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="c48f5-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c48f5-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="c48f5-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c48f5-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="c48f5-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c48f5-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
