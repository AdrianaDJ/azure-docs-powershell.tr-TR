---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274076"
---
# <span data-ttu-id="6d94e-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6d94e-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="6d94e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d94e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d94e-103">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d94e-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="6d94e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d94e-104">SYNTAX</span></span>

### <span data-ttu-id="6d94e-105">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d94e-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d94e-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6d94e-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d94e-107">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="6d94e-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d94e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d94e-108">DESCRIPTION</span></span>
<span data-ttu-id="6d94e-109">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d94e-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="6d94e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d94e-110">EXAMPLES</span></span>

### <span data-ttu-id="6d94e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6d94e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="6d94e-112">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="6d94e-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="6d94e-113">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d94e-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="6d94e-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6d94e-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="6d94e-115">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="6d94e-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="6d94e-116">Bu silme işlemi, yeni-AzVirtualWan tarafından döndürülen sanal WAN nesnesini kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="6d94e-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="6d94e-117">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d94e-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="6d94e-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6d94e-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="6d94e-119">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="6d94e-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="6d94e-120">Bu silme işlemi, yeni-AzVirtualWan tarafından döndürülen sanal WAN kaynak kimliğini kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="6d94e-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="6d94e-121">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d94e-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="6d94e-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d94e-122">PARAMETERS</span></span>

### <span data-ttu-id="6d94e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d94e-123">-DefaultProfile</span></span>
<span data-ttu-id="6d94e-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d94e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d94e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6d94e-125">-Force</span></span>
<span data-ttu-id="6d94e-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="6d94e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6d94e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d94e-127">-InputObject</span></span>
<span data-ttu-id="6d94e-128">Silinecek sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6d94e-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="6d94e-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d94e-129">-Name</span></span>
<span data-ttu-id="6d94e-130">Sanal WAN adı.</span><span class="sxs-lookup"><span data-stu-id="6d94e-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="6d94e-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6d94e-131">-PassThru</span></span>
<span data-ttu-id="6d94e-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6d94e-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6d94e-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6d94e-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6d94e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d94e-134">-ResourceGroupName</span></span>
<span data-ttu-id="6d94e-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6d94e-135">The resource group name.</span></span>

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

### <span data-ttu-id="6d94e-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6d94e-136">-ResourceId</span></span>
<span data-ttu-id="6d94e-137">Silinecek sanal WAN için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6d94e-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="6d94e-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d94e-138">-Confirm</span></span>
<span data-ttu-id="6d94e-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d94e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d94e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d94e-140">-WhatIf</span></span>
<span data-ttu-id="6d94e-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d94e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d94e-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d94e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d94e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d94e-143">CommonParameters</span></span>
<span data-ttu-id="6d94e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d94e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d94e-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d94e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d94e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d94e-146">INPUTS</span></span>

### <span data-ttu-id="6d94e-147">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6d94e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="6d94e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6d94e-148">System.String</span></span>

## <span data-ttu-id="6d94e-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d94e-149">OUTPUTS</span></span>

### <span data-ttu-id="6d94e-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d94e-150">System.Boolean</span></span>

## <span data-ttu-id="6d94e-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d94e-151">NOTES</span></span>

## <span data-ttu-id="6d94e-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d94e-152">RELATED LINKS</span></span>

[<span data-ttu-id="6d94e-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6d94e-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="6d94e-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6d94e-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="6d94e-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6d94e-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
