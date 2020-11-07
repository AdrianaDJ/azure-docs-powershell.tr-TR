---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760128"
---
# <span data-ttu-id="f9500-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f9500-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="f9500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9500-102">SYNOPSIS</span></span>
<span data-ttu-id="f9500-103">Genel IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="f9500-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="f9500-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9500-104">SYNTAX</span></span>

### <span data-ttu-id="f9500-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9500-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9500-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f9500-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9500-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9500-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9500-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9500-108">DESCRIPTION</span></span>
<span data-ttu-id="f9500-109">**Remove-Azpublicıpprefix** cmdlet 'i, kendisinden herhangi BIR genel IP adresi olmadığı sürece bir Azure genel IP önekini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9500-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="f9500-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9500-110">EXAMPLES</span></span>

### <span data-ttu-id="f9500-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f9500-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="f9500-112">$prefixName $rgName kaynak grubundan ortak IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="f9500-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="f9500-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9500-113">PARAMETERS</span></span>

### <span data-ttu-id="f9500-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="f9500-114">-AsJob</span></span>
<span data-ttu-id="f9500-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f9500-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9500-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9500-116">-DefaultProfile</span></span>
<span data-ttu-id="f9500-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9500-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9500-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f9500-118">-Force</span></span>
<span data-ttu-id="f9500-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="f9500-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9500-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9500-120">-InputObject</span></span>
<span data-ttu-id="f9500-121">Publicıpprefix nesnesi</span><span class="sxs-lookup"><span data-stu-id="f9500-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="f9500-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9500-122">-Name</span></span>
<span data-ttu-id="f9500-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f9500-123">The resource name.</span></span>

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

### <span data-ttu-id="f9500-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f9500-124">-PassThru</span></span>
<span data-ttu-id="f9500-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9500-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f9500-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f9500-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9500-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9500-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9500-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f9500-128">The resource group name.</span></span>

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

### <span data-ttu-id="f9500-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f9500-129">-ResourceId</span></span>
<span data-ttu-id="f9500-130">Kaldırılacak kaynağın RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f9500-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="f9500-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9500-131">-Confirm</span></span>
<span data-ttu-id="f9500-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9500-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9500-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9500-133">-WhatIf</span></span>
<span data-ttu-id="f9500-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9500-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9500-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9500-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9500-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9500-136">CommonParameters</span></span>
<span data-ttu-id="f9500-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9500-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9500-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9500-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9500-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9500-139">INPUTS</span></span>

### <span data-ttu-id="f9500-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f9500-140">System.String</span></span>

### <span data-ttu-id="f9500-141">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f9500-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="f9500-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9500-142">OUTPUTS</span></span>

### <span data-ttu-id="f9500-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9500-143">System.Boolean</span></span>

## <span data-ttu-id="f9500-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9500-144">NOTES</span></span>

## <span data-ttu-id="f9500-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9500-145">RELATED LINKS</span></span>

[<span data-ttu-id="f9500-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f9500-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="f9500-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f9500-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="f9500-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f9500-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
