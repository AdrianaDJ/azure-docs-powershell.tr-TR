---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: c620c2f927fa5de60a637f45e8f0ff64f2a25b27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760112"
---
# <span data-ttu-id="5213b-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5213b-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="5213b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5213b-102">SYNOPSIS</span></span>
<span data-ttu-id="5213b-103">Bir Azure VirtualHub kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5213b-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="5213b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5213b-104">SYNTAX</span></span>

### <span data-ttu-id="5213b-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5213b-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5213b-106">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="5213b-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5213b-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="5213b-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5213b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5213b-108">DESCRIPTION</span></span>
<span data-ttu-id="5213b-109">Bir Azure VirtualHub kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5213b-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="5213b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5213b-110">EXAMPLES</span></span>

### <span data-ttu-id="5213b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5213b-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="5213b-112">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5213b-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="5213b-113">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5213b-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="5213b-114">Ardından, bu sanal hub 'ı ResourceGroupName ve ResourceName kullanarak siler.</span><span class="sxs-lookup"><span data-stu-id="5213b-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="5213b-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5213b-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="5213b-116">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5213b-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="5213b-117">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5213b-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="5213b-118">Ardından, bir giriş nesnesi kullanarak sanal hub 'ı siler.</span><span class="sxs-lookup"><span data-stu-id="5213b-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="5213b-119">Giriş nesnesi PSVirtualHub türünde.</span><span class="sxs-lookup"><span data-stu-id="5213b-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="5213b-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5213b-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="5213b-121">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5213b-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="5213b-122">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5213b-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="5213b-123">Ardından Get-AzVirtualHub 'dan çıktı kullanarak PowerShell boruları kullanarak sanal hub 'ı siler.</span><span class="sxs-lookup"><span data-stu-id="5213b-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="5213b-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5213b-124">PARAMETERS</span></span>

### <span data-ttu-id="5213b-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="5213b-125">-AsJob</span></span>
<span data-ttu-id="5213b-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5213b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5213b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5213b-127">-DefaultProfile</span></span>
<span data-ttu-id="5213b-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5213b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5213b-129">-Force</span><span class="sxs-lookup"><span data-stu-id="5213b-129">-Force</span></span>
<span data-ttu-id="5213b-130">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="5213b-130">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="5213b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5213b-131">-InputObject</span></span>
<span data-ttu-id="5213b-132">Değiştirilecek sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5213b-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5213b-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="5213b-133">-Name</span></span>
<span data-ttu-id="5213b-134">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="5213b-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5213b-135">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5213b-135">-PassThru</span></span>
<span data-ttu-id="5213b-136">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5213b-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5213b-137">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5213b-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5213b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5213b-138">-ResourceGroupName</span></span>
<span data-ttu-id="5213b-139">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5213b-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5213b-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5213b-140">-ResourceId</span></span>
<span data-ttu-id="5213b-141">Değiştirilecek sanal hub 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5213b-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5213b-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="5213b-142">-Confirm</span></span>
<span data-ttu-id="5213b-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5213b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5213b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5213b-144">-WhatIf</span></span>
<span data-ttu-id="5213b-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5213b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5213b-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5213b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5213b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5213b-147">CommonParameters</span></span>
<span data-ttu-id="5213b-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5213b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5213b-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5213b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5213b-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5213b-150">INPUTS</span></span>

### <span data-ttu-id="5213b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5213b-151">System.String</span></span>

### <span data-ttu-id="5213b-152">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5213b-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="5213b-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5213b-153">OUTPUTS</span></span>

### <span data-ttu-id="5213b-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5213b-154">System.Boolean</span></span>

## <span data-ttu-id="5213b-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5213b-155">NOTES</span></span>

## <span data-ttu-id="5213b-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5213b-156">RELATED LINKS</span></span>

[<span data-ttu-id="5213b-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5213b-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="5213b-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5213b-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="5213b-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5213b-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
