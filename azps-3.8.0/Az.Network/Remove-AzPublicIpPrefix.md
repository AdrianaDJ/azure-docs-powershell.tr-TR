---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104003"
---
# <span data-ttu-id="770e6-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="770e6-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="770e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770e6-102">SYNOPSIS</span></span>
<span data-ttu-id="770e6-103">Genel IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="770e6-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="770e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="770e6-104">SYNTAX</span></span>

### <span data-ttu-id="770e6-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="770e6-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770e6-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="770e6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770e6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="770e6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770e6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="770e6-108">DESCRIPTION</span></span>
<span data-ttu-id="770e6-109">**Remove-Azpublicıpprefix** cmdlet 'i, kendisinden herhangi BIR genel IP adresi olmadığı sürece bir Azure genel IP önekini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="770e6-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="770e6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="770e6-110">EXAMPLES</span></span>

### <span data-ttu-id="770e6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="770e6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="770e6-112">$prefixName $rgName kaynak grubundan ortak IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="770e6-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="770e6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="770e6-113">PARAMETERS</span></span>

### <span data-ttu-id="770e6-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="770e6-114">-AsJob</span></span>
<span data-ttu-id="770e6-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="770e6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="770e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770e6-116">-DefaultProfile</span></span>
<span data-ttu-id="770e6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="770e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770e6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="770e6-118">-Force</span></span>
<span data-ttu-id="770e6-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="770e6-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="770e6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770e6-120">-InputObject</span></span>
<span data-ttu-id="770e6-121">Publicıpprefix nesnesi</span><span class="sxs-lookup"><span data-stu-id="770e6-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="770e6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="770e6-122">-Name</span></span>
<span data-ttu-id="770e6-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="770e6-123">The resource name.</span></span>

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

### <span data-ttu-id="770e6-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="770e6-124">-PassThru</span></span>
<span data-ttu-id="770e6-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="770e6-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="770e6-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="770e6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="770e6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770e6-127">-ResourceGroupName</span></span>
<span data-ttu-id="770e6-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="770e6-128">The resource group name.</span></span>

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

### <span data-ttu-id="770e6-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="770e6-129">-ResourceId</span></span>
<span data-ttu-id="770e6-130">Kaldırılacak kaynağın RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="770e6-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="770e6-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="770e6-131">-Confirm</span></span>
<span data-ttu-id="770e6-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="770e6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770e6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770e6-133">-WhatIf</span></span>
<span data-ttu-id="770e6-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="770e6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770e6-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="770e6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770e6-136">CommonParameters</span></span>
<span data-ttu-id="770e6-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="770e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770e6-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770e6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770e6-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="770e6-139">INPUTS</span></span>

### <span data-ttu-id="770e6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="770e6-140">System.String</span></span>

### <span data-ttu-id="770e6-141">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="770e6-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="770e6-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="770e6-142">OUTPUTS</span></span>

### <span data-ttu-id="770e6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="770e6-143">System.Boolean</span></span>

## <span data-ttu-id="770e6-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="770e6-144">NOTES</span></span>

## <span data-ttu-id="770e6-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="770e6-145">RELATED LINKS</span></span>

[<span data-ttu-id="770e6-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="770e6-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="770e6-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="770e6-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="770e6-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="770e6-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
