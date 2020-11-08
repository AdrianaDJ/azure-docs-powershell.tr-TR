---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274349"
---
# <span data-ttu-id="120ea-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="120ea-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="120ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120ea-102">SYNOPSIS</span></span>
<span data-ttu-id="120ea-103">VirtualHub ile ilişkili bir hub yol tablosu kaynağını silme.</span><span class="sxs-lookup"><span data-stu-id="120ea-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="120ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="120ea-104">SYNTAX</span></span>

### <span data-ttu-id="120ea-105">ByVHubRouteTableName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="120ea-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="120ea-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="120ea-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="120ea-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="120ea-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="120ea-108">Byvhubroutetableresourceıd</span><span class="sxs-lookup"><span data-stu-id="120ea-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120ea-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="120ea-109">DESCRIPTION</span></span>
<span data-ttu-id="120ea-110">Belirtilen sanal hub ile ilişkili belirtilen hub yol tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="120ea-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="120ea-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="120ea-111">EXAMPLES</span></span>

### <span data-ttu-id="120ea-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="120ea-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="120ea-113">Bu komut sanal hub 'ın hub yol tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="120ea-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="120ea-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="120ea-114">PARAMETERS</span></span>

### <span data-ttu-id="120ea-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="120ea-115">-AsJob</span></span>
<span data-ttu-id="120ea-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="120ea-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="120ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120ea-117">-DefaultProfile</span></span>
<span data-ttu-id="120ea-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="120ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="120ea-119">-Force</span><span class="sxs-lookup"><span data-stu-id="120ea-119">-Force</span></span>
<span data-ttu-id="120ea-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="120ea-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="120ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="120ea-121">-InputObject</span></span>
<span data-ttu-id="120ea-122">Kaldırılacak vhubroutetable kaynağı.</span><span class="sxs-lookup"><span data-stu-id="120ea-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="120ea-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="120ea-123">-Name</span></span>
<span data-ttu-id="120ea-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="120ea-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ea-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="120ea-125">-ParentObject</span></span>
<span data-ttu-id="120ea-126">Bu kaynağın üst sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="120ea-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="120ea-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="120ea-127">-ParentResourceName</span></span>
<span data-ttu-id="120ea-128">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="120ea-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ea-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="120ea-129">-PassThru</span></span>
<span data-ttu-id="120ea-130">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="120ea-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="120ea-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="120ea-131">-ResourceGroupName</span></span>
<span data-ttu-id="120ea-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="120ea-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ea-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="120ea-133">-ResourceId</span></span>
<span data-ttu-id="120ea-134">Kaldırılacak vhubroutetable kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="120ea-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="120ea-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="120ea-135">-Confirm</span></span>
<span data-ttu-id="120ea-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="120ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120ea-137">-WhatIf</span></span>
<span data-ttu-id="120ea-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="120ea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120ea-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="120ea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120ea-140">CommonParameters</span></span>
<span data-ttu-id="120ea-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="120ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120ea-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="120ea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120ea-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="120ea-143">INPUTS</span></span>

### <span data-ttu-id="120ea-144">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="120ea-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="120ea-145">Microsoft. Azure. Commands. Network. model. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="120ea-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="120ea-146">System. String</span><span class="sxs-lookup"><span data-stu-id="120ea-146">System.String</span></span>

## <span data-ttu-id="120ea-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="120ea-147">OUTPUTS</span></span>

### <span data-ttu-id="120ea-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="120ea-148">System.Boolean</span></span>

## <span data-ttu-id="120ea-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="120ea-149">NOTES</span></span>

## <span data-ttu-id="120ea-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="120ea-150">RELATED LINKS</span></span>

[<span data-ttu-id="120ea-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="120ea-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="120ea-152">Yeni-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="120ea-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="120ea-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="120ea-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="120ea-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="120ea-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)