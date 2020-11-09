---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325246"
---
# <span data-ttu-id="0861b-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0861b-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="0861b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0861b-102">SYNOPSIS</span></span>
<span data-ttu-id="0861b-103">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0861b-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="0861b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0861b-104">SYNTAX</span></span>

### <span data-ttu-id="0861b-105">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0861b-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0861b-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0861b-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0861b-107">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="0861b-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0861b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0861b-108">DESCRIPTION</span></span>
<span data-ttu-id="0861b-109">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0861b-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="0861b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0861b-110">EXAMPLES</span></span>

### <span data-ttu-id="0861b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0861b-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="0861b-112">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="0861b-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0861b-113">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0861b-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="0861b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0861b-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="0861b-115">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="0861b-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0861b-116">Bu silme işlemi, yeni-AzVirtualWan tarafından döndürülen sanal WAN nesnesini kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="0861b-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="0861b-117">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0861b-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="0861b-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0861b-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="0861b-119">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="0861b-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0861b-120">Bu silme işlemi, yeni-AzVirtualWan tarafından döndürülen sanal WAN kaynak kimliğini kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="0861b-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="0861b-121">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0861b-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="0861b-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0861b-122">PARAMETERS</span></span>

### <span data-ttu-id="0861b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0861b-123">-DefaultProfile</span></span>
<span data-ttu-id="0861b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0861b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0861b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0861b-125">-Force</span></span>
<span data-ttu-id="0861b-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="0861b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0861b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0861b-127">-InputObject</span></span>
<span data-ttu-id="0861b-128">Silinecek sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0861b-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="0861b-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="0861b-129">-Name</span></span>
<span data-ttu-id="0861b-130">Sanal WAN adı.</span><span class="sxs-lookup"><span data-stu-id="0861b-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="0861b-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0861b-131">-PassThru</span></span>
<span data-ttu-id="0861b-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0861b-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0861b-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0861b-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0861b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0861b-134">-ResourceGroupName</span></span>
<span data-ttu-id="0861b-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0861b-135">The resource group name.</span></span>

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

### <span data-ttu-id="0861b-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0861b-136">-ResourceId</span></span>
<span data-ttu-id="0861b-137">Silinecek sanal WAN için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0861b-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="0861b-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="0861b-138">-Confirm</span></span>
<span data-ttu-id="0861b-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0861b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0861b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0861b-140">-WhatIf</span></span>
<span data-ttu-id="0861b-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0861b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0861b-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0861b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0861b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0861b-143">CommonParameters</span></span>
<span data-ttu-id="0861b-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0861b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0861b-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0861b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0861b-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0861b-146">INPUTS</span></span>

### <span data-ttu-id="0861b-147">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0861b-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="0861b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0861b-148">System.String</span></span>

## <span data-ttu-id="0861b-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0861b-149">OUTPUTS</span></span>

### <span data-ttu-id="0861b-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0861b-150">System.Boolean</span></span>

## <span data-ttu-id="0861b-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0861b-151">NOTES</span></span>

## <span data-ttu-id="0861b-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0861b-152">RELATED LINKS</span></span>

[<span data-ttu-id="0861b-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0861b-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="0861b-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0861b-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="0861b-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0861b-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
