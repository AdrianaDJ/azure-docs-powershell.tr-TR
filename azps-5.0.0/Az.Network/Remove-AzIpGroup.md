---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276084"
---
# <span data-ttu-id="609be-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="609be-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="609be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="609be-102">SYNOPSIS</span></span>
<span data-ttu-id="609be-103">Bir Azure ıpgroup siler.</span><span class="sxs-lookup"><span data-stu-id="609be-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="609be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="609be-104">SYNTAX</span></span>

### <span data-ttu-id="609be-105">Ipgroupnameparameterset</span><span class="sxs-lookup"><span data-stu-id="609be-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="609be-106">Ipgroupınputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="609be-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="609be-107">Ipgroupresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="609be-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="609be-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="609be-108">DESCRIPTION</span></span>
<span data-ttu-id="609be-109">**Remove-Azıpgroup** cmdlet 'ı bir Azure ıpgroup 'u siler</span><span class="sxs-lookup"><span data-stu-id="609be-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="609be-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="609be-110">EXAMPLES</span></span>

### <span data-ttu-id="609be-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="609be-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="609be-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="609be-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="609be-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="609be-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="609be-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="609be-114">PARAMETERS</span></span>

### <span data-ttu-id="609be-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="609be-115">-AsJob</span></span>
<span data-ttu-id="609be-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="609be-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="609be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609be-117">-DefaultProfile</span></span>
<span data-ttu-id="609be-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="609be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="609be-119">-Force</span><span class="sxs-lookup"><span data-stu-id="609be-119">-Force</span></span>
<span data-ttu-id="609be-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="609be-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="609be-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="609be-121">-IpGroup</span></span>
<span data-ttu-id="609be-122">Ipgroup giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="609be-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="609be-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="609be-123">-Name</span></span>
<span data-ttu-id="609be-124">Ipgroup 'un adı.</span><span class="sxs-lookup"><span data-stu-id="609be-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609be-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="609be-125">-PassThru</span></span>
<span data-ttu-id="609be-126">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="609be-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="609be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="609be-127">-ResourceGroupName</span></span>
<span data-ttu-id="609be-128">Ipgroup 'un kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="609be-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609be-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="609be-129">-ResourceId</span></span>
<span data-ttu-id="609be-130">Ipgroup kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="609be-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609be-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="609be-131">-Confirm</span></span>
<span data-ttu-id="609be-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="609be-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="609be-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="609be-133">-WhatIf</span></span>
<span data-ttu-id="609be-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="609be-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="609be-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="609be-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="609be-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609be-136">CommonParameters</span></span>
<span data-ttu-id="609be-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="609be-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609be-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="609be-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609be-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="609be-139">INPUTS</span></span>

### <span data-ttu-id="609be-140">System. String</span><span class="sxs-lookup"><span data-stu-id="609be-140">System.String</span></span>

### <span data-ttu-id="609be-141">Microsoft. Azure. Commands. Network. model. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="609be-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="609be-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="609be-142">OUTPUTS</span></span>

### <span data-ttu-id="609be-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="609be-143">System.Boolean</span></span>

## <span data-ttu-id="609be-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="609be-144">NOTES</span></span>

## <span data-ttu-id="609be-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="609be-145">RELATED LINKS</span></span>
