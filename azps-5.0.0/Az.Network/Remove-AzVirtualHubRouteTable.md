---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278098"
---
# <span data-ttu-id="027d3-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="027d3-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="027d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="027d3-102">SYNOPSIS</span></span>
<span data-ttu-id="027d3-103">Sanal hub ile ilişkili sanal hub yol tablosu kaynağını silme.</span><span class="sxs-lookup"><span data-stu-id="027d3-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="027d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="027d3-104">SYNTAX</span></span>

### <span data-ttu-id="027d3-105">ByVirtualHubRouteTableName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="027d3-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="027d3-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="027d3-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="027d3-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="027d3-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="027d3-108">Byvirtualhubroutetableresourceıd</span><span class="sxs-lookup"><span data-stu-id="027d3-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="027d3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="027d3-109">DESCRIPTION</span></span>
<span data-ttu-id="027d3-110">Belirtilen sanal hub ile ilişkili belirtilen yol tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="027d3-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="027d3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="027d3-111">EXAMPLES</span></span>

### <span data-ttu-id="027d3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="027d3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="027d3-113">Bu komut, sanal hub westushub routeTable1 siler.</span><span class="sxs-lookup"><span data-stu-id="027d3-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="027d3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="027d3-114">PARAMETERS</span></span>

### <span data-ttu-id="027d3-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="027d3-115">-AsJob</span></span>
<span data-ttu-id="027d3-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="027d3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="027d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027d3-117">-DefaultProfile</span></span>
<span data-ttu-id="027d3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="027d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="027d3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="027d3-119">-Force</span></span>
<span data-ttu-id="027d3-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="027d3-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="027d3-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="027d3-121">-HubName</span></span>
<span data-ttu-id="027d3-122">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="027d3-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="027d3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="027d3-123">-InputObject</span></span>
<span data-ttu-id="027d3-124">Kaldırılacak virtualhubroutetable kaynağı.</span><span class="sxs-lookup"><span data-stu-id="027d3-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="027d3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="027d3-125">-Name</span></span>
<span data-ttu-id="027d3-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="027d3-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="027d3-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="027d3-127">-PassThru</span></span>
<span data-ttu-id="027d3-128">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="027d3-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="027d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="027d3-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="027d3-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="027d3-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="027d3-131">-ResourceId</span></span>
<span data-ttu-id="027d3-132">Kaldırılacak virtualhubroutetable kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="027d3-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="027d3-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="027d3-133">-VirtualHub</span></span>
<span data-ttu-id="027d3-134">{{VirtualHub açıklamasını doldurun}}</span><span class="sxs-lookup"><span data-stu-id="027d3-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="027d3-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="027d3-135">-Confirm</span></span>
<span data-ttu-id="027d3-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="027d3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="027d3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="027d3-137">-WhatIf</span></span>
<span data-ttu-id="027d3-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="027d3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="027d3-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="027d3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="027d3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027d3-140">CommonParameters</span></span>
<span data-ttu-id="027d3-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="027d3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027d3-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="027d3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027d3-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="027d3-143">INPUTS</span></span>

### <span data-ttu-id="027d3-144">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="027d3-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="027d3-145">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="027d3-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="027d3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="027d3-146">System.String</span></span>

## <span data-ttu-id="027d3-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="027d3-147">OUTPUTS</span></span>

### <span data-ttu-id="027d3-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="027d3-148">System.Boolean</span></span>

## <span data-ttu-id="027d3-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="027d3-149">NOTES</span></span>

## <span data-ttu-id="027d3-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="027d3-150">RELATED LINKS</span></span>
