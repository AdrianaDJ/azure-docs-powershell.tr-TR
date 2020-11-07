---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764331"
---
# <span data-ttu-id="fb838-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fb838-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="fb838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb838-102">SYNOPSIS</span></span>
<span data-ttu-id="fb838-103">Genel IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="fb838-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb838-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb838-104">SYNTAX</span></span>

### <span data-ttu-id="fb838-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb838-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb838-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fb838-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb838-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb838-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb838-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb838-108">DESCRIPTION</span></span>
<span data-ttu-id="fb838-109">\* \* Remove-AzureRmPublicIpPrefix cmdlet 'i, kendisinden herhangi bir genel IP adresi olmadığı sürece bir Azure genel IP önekini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb838-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="fb838-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb838-110">EXAMPLES</span></span>

### <span data-ttu-id="fb838-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb838-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="fb838-112">$prefixName $rgName kaynak grubundan ortak IP önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="fb838-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="fb838-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb838-113">PARAMETERS</span></span>

### <span data-ttu-id="fb838-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="fb838-114">-AsJob</span></span>
<span data-ttu-id="fb838-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fb838-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb838-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb838-116">-DefaultProfile</span></span>
<span data-ttu-id="fb838-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb838-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb838-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fb838-118">-Force</span></span>
<span data-ttu-id="fb838-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="fb838-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fb838-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb838-120">-InputObject</span></span>
<span data-ttu-id="fb838-121">Publicıpprefix nesnesi</span><span class="sxs-lookup"><span data-stu-id="fb838-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb838-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb838-122">-Name</span></span>
<span data-ttu-id="fb838-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="fb838-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb838-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb838-124">-PassThru</span></span>
<span data-ttu-id="fb838-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fb838-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb838-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fb838-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb838-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb838-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb838-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fb838-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb838-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb838-129">-ResourceId</span></span>
<span data-ttu-id="fb838-130">Kaldırılacak kaynağın RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb838-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="fb838-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb838-131">-Confirm</span></span>
<span data-ttu-id="fb838-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb838-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb838-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb838-133">-WhatIf</span></span>
<span data-ttu-id="fb838-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb838-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb838-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb838-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb838-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb838-136">CommonParameters</span></span>
<span data-ttu-id="fb838-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb838-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fb838-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb838-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb838-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb838-139">INPUTS</span></span>

### <span data-ttu-id="fb838-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fb838-140">System.String</span></span>
<span data-ttu-id="fb838-141">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fb838-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="fb838-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb838-142">OUTPUTS</span></span>

### <span data-ttu-id="fb838-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="fb838-143">System.Object</span></span>

## <span data-ttu-id="fb838-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb838-144">NOTES</span></span>

## <span data-ttu-id="fb838-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb838-145">RELATED LINKS</span></span>
