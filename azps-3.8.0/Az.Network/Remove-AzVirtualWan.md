---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103963"
---
# <span data-ttu-id="595d8-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="595d8-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="595d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595d8-102">SYNOPSIS</span></span>
<span data-ttu-id="595d8-103">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="595d8-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="595d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="595d8-104">SYNTAX</span></span>

### <span data-ttu-id="595d8-105">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="595d8-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="595d8-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="595d8-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="595d8-107">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="595d8-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595d8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="595d8-108">DESCRIPTION</span></span>
<span data-ttu-id="595d8-109">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="595d8-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="595d8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="595d8-110">EXAMPLES</span></span>

### <span data-ttu-id="595d8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="595d8-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="595d8-112">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="595d8-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="595d8-113">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="595d8-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="595d8-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="595d8-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="595d8-115">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="595d8-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="595d8-116">Bu silme işlemi, yeni-AzVirtualWan tarafından döndürülen sanal WAN nesnesini kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="595d8-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="595d8-117">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="595d8-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="595d8-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="595d8-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="595d8-119">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="595d8-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="595d8-120">Bu silme işlemi, yeni-AzVirtualWan tarafından döndürülen sanal WAN kaynak kimliğini kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="595d8-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="595d8-121">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="595d8-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="595d8-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="595d8-122">PARAMETERS</span></span>

### <span data-ttu-id="595d8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595d8-123">-DefaultProfile</span></span>
<span data-ttu-id="595d8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="595d8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="595d8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="595d8-125">-Force</span></span>
<span data-ttu-id="595d8-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="595d8-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="595d8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="595d8-127">-InputObject</span></span>
<span data-ttu-id="595d8-128">Silinecek sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="595d8-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="595d8-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="595d8-129">-Name</span></span>
<span data-ttu-id="595d8-130">Sanal WAN adı.</span><span class="sxs-lookup"><span data-stu-id="595d8-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595d8-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="595d8-131">-PassThru</span></span>
<span data-ttu-id="595d8-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="595d8-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="595d8-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="595d8-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="595d8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595d8-134">-ResourceGroupName</span></span>
<span data-ttu-id="595d8-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="595d8-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595d8-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="595d8-136">-ResourceId</span></span>
<span data-ttu-id="595d8-137">Silinecek sanal WAN için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="595d8-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595d8-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="595d8-138">-Confirm</span></span>
<span data-ttu-id="595d8-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="595d8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="595d8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595d8-140">-WhatIf</span></span>
<span data-ttu-id="595d8-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="595d8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="595d8-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="595d8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="595d8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595d8-143">CommonParameters</span></span>
<span data-ttu-id="595d8-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="595d8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595d8-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="595d8-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595d8-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="595d8-146">INPUTS</span></span>

### <span data-ttu-id="595d8-147">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="595d8-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="595d8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="595d8-148">System.String</span></span>

## <span data-ttu-id="595d8-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="595d8-149">OUTPUTS</span></span>

### <span data-ttu-id="595d8-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="595d8-150">System.Boolean</span></span>

## <span data-ttu-id="595d8-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="595d8-151">NOTES</span></span>

## <span data-ttu-id="595d8-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="595d8-152">RELATED LINKS</span></span>

[<span data-ttu-id="595d8-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="595d8-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="595d8-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="595d8-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="595d8-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="595d8-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
