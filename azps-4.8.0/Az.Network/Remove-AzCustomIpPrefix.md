---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274348"
---
# <span data-ttu-id="2b7b8-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2b7b8-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="2b7b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7b8-103">Custobir önek kaldırır</span><span class="sxs-lookup"><span data-stu-id="2b7b8-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="2b7b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b7b8-104">SYNTAX</span></span>

### <span data-ttu-id="2b7b8-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b7b8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b7b8-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2b7b8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b7b8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b7b8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b7b8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b7b8-108">DESCRIPTION</span></span>
<span data-ttu-id="2b7b8-109">**Remove-Azcustomhttp öneki** cmdlet 'ı bir custobir önek kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="2b7b8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b7b8-110">EXAMPLES</span></span>

### <span data-ttu-id="2b7b8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b7b8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="2b7b8-112">$PrefixName $RgName kaynak grubundan kaldır</span><span class="sxs-lookup"><span data-stu-id="2b7b8-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="2b7b8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b7b8-113">PARAMETERS</span></span>

### <span data-ttu-id="2b7b8-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="2b7b8-114">-AsJob</span></span>
<span data-ttu-id="2b7b8-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2b7b8-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b8-116">-DefaultProfile</span></span>
<span data-ttu-id="2b7b8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2b7b8-118">-Force</span></span>
<span data-ttu-id="2b7b8-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b7b8-120">-InputObject</span></span>
<span data-ttu-id="2b7b8-121">Custobir önek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b7b8-122">-Name</span></span>
<span data-ttu-id="2b7b8-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2b7b8-124">-PassThru</span></span>
<span data-ttu-id="2b7b8-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2b7b8-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="2b7b8-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2b7b8-129">-ResourceId</span></span>
<span data-ttu-id="2b7b8-130">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b7b8-131">-Confirm</span></span>
<span data-ttu-id="2b7b8-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7b8-133">-WhatIf</span></span>
<span data-ttu-id="2b7b8-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7b8-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7b8-136">CommonParameters</span></span>
<span data-ttu-id="2b7b8-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7b8-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7b8-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b7b8-139">INPUTS</span></span>

### <span data-ttu-id="2b7b8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2b7b8-140">System.String</span></span>

### <span data-ttu-id="2b7b8-141">Microsoft. Azure. Commands. Network. model. Pscustolermi öneki</span><span class="sxs-lookup"><span data-stu-id="2b7b8-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="2b7b8-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b7b8-142">OUTPUTS</span></span>

### <span data-ttu-id="2b7b8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b7b8-143">System.Boolean</span></span>

## <span data-ttu-id="2b7b8-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b7b8-144">NOTES</span></span>

## <span data-ttu-id="2b7b8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b7b8-145">RELATED LINKS</span></span>

[<span data-ttu-id="2b7b8-146">Get-Azözelmi öneki</span><span class="sxs-lookup"><span data-stu-id="2b7b8-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="2b7b8-147">Yeni-Azözelmi öneki</span><span class="sxs-lookup"><span data-stu-id="2b7b8-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="2b7b8-148">Update-Azcustombu önek</span><span class="sxs-lookup"><span data-stu-id="2b7b8-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)