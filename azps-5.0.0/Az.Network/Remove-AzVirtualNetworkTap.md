---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278822"
---
# <span data-ttu-id="1d71a-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1d71a-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="1d71a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d71a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d71a-103">Sanal bir ağ öğesine dokunun.</span><span class="sxs-lookup"><span data-stu-id="1d71a-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="1d71a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d71a-104">SYNTAX</span></span>

### <span data-ttu-id="1d71a-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1d71a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d71a-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1d71a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d71a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d71a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d71a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d71a-108">DESCRIPTION</span></span>
<span data-ttu-id="1d71a-109">**Remove-AzVirtualNetworkTap** cmdlet 'ı bir Azure sanal ağ öğesine dokunun.</span><span class="sxs-lookup"><span data-stu-id="1d71a-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="1d71a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d71a-110">EXAMPLES</span></span>

### <span data-ttu-id="1d71a-111">Örnek 1: sanal ağ 'ı kaldırma</span><span class="sxs-lookup"><span data-stu-id="1d71a-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="1d71a-112">Bu komut ResourceGroup1 kaynak grubundaki VirtualNetworkTap1 kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d71a-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1d71a-113">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="1d71a-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="1d71a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d71a-114">PARAMETERS</span></span>

### <span data-ttu-id="1d71a-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1d71a-115">-AsJob</span></span>
<span data-ttu-id="1d71a-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1d71a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d71a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d71a-117">-DefaultProfile</span></span>
<span data-ttu-id="1d71a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d71a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d71a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1d71a-119">-Force</span></span>
<span data-ttu-id="1d71a-120">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="1d71a-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="1d71a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d71a-121">-InputObject</span></span>
<span data-ttu-id="1d71a-122">VirtualNetworkTap kaynağına başvuru</span><span class="sxs-lookup"><span data-stu-id="1d71a-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d71a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d71a-123">-Name</span></span>
<span data-ttu-id="1d71a-124">Dokunun adı.</span><span class="sxs-lookup"><span data-stu-id="1d71a-124">The name of the tap.</span></span>

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

### <span data-ttu-id="1d71a-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1d71a-125">-PassThru</span></span>
<span data-ttu-id="1d71a-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1d71a-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1d71a-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1d71a-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1d71a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d71a-128">-ResourceGroupName</span></span>
<span data-ttu-id="1d71a-129">Sanal ağın kaynak grup adı dokunun.</span><span class="sxs-lookup"><span data-stu-id="1d71a-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="1d71a-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1d71a-130">-ResourceId</span></span>
<span data-ttu-id="1d71a-131">VirtualNetworkTap RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1d71a-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="1d71a-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d71a-132">-Confirm</span></span>
<span data-ttu-id="1d71a-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d71a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d71a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d71a-134">-WhatIf</span></span>
<span data-ttu-id="1d71a-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d71a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d71a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d71a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d71a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d71a-137">CommonParameters</span></span>
<span data-ttu-id="1d71a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d71a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d71a-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d71a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d71a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d71a-140">INPUTS</span></span>

### <span data-ttu-id="1d71a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1d71a-141">System.String</span></span>

### <span data-ttu-id="1d71a-142">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1d71a-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="1d71a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d71a-143">OUTPUTS</span></span>

### <span data-ttu-id="1d71a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d71a-144">System.Boolean</span></span>

## <span data-ttu-id="1d71a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d71a-145">NOTES</span></span>

## <span data-ttu-id="1d71a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d71a-146">RELATED LINKS</span></span>

[<span data-ttu-id="1d71a-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1d71a-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="1d71a-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1d71a-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="1d71a-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1d71a-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
