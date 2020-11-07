---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937040"
---
# <span data-ttu-id="59995-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="59995-101">Get-AzVM</span></span>

## <span data-ttu-id="59995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59995-102">SYNOPSIS</span></span>
<span data-ttu-id="59995-103">Sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="59995-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="59995-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59995-104">SYNTAX</span></span>

### <span data-ttu-id="59995-105">Listallvirtual, Inesparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59995-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59995-106">Listvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="59995-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59995-107">Getvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="59995-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59995-108">Listnextlinkvirtual, Inesparamset</span><span class="sxs-lookup"><span data-stu-id="59995-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59995-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="59995-109">DESCRIPTION</span></span>
<span data-ttu-id="59995-110">**Get-azıvm** cmdlet 'i, bir Azure sanal makinesinin model görünümünü ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="59995-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="59995-111">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="59995-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="59995-112">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="59995-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="59995-113">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="59995-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="59995-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59995-114">EXAMPLES</span></span>

### <span data-ttu-id="59995-115">Örnek 1: model ve örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="59995-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="59995-116">Bu komut, VirtualMachine07 adındaki sanal makinenin model görünümü ve örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="59995-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="59995-117">Örnek 2: örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="59995-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="59995-118">Bu komut, VirtualMachine07 adındaki sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="59995-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="59995-119">Bu komut, *Status* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59995-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="59995-120">Bu nedenle, komut yalnızca örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="59995-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="59995-121">Örnek 3: kaynak grubundaki tüm sanal makinelerin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="59995-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="59995-122">Bu komut, ResourceGroup11 adlı kaynak grubundaki tüm sanal makinelerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="59995-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="59995-123">Örnek 4: aboneliğinizdeki tüm sanal makineleri edinme</span><span class="sxs-lookup"><span data-stu-id="59995-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="59995-124">Bu komut aboneliğinizdeki tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="59995-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="59995-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59995-125">PARAMETERS</span></span>

### <span data-ttu-id="59995-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59995-126">-DefaultProfile</span></span>
<span data-ttu-id="59995-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59995-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59995-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="59995-128">-DisplayHint</span></span>
<span data-ttu-id="59995-129">Sanal makine nesnesinin nasıl görüntülendiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="59995-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="59995-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="59995-130">Valid values are:</span></span>

<span data-ttu-id="59995-131">--Compact: yalnızca üst düzey özelliklerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="59995-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="59995-132">--Genişlet: tüm düzeylerdeki tüm özellikleri görüntüler</span><span class="sxs-lookup"><span data-stu-id="59995-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59995-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="59995-133">-Name</span></span>
<span data-ttu-id="59995-134">Alınacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59995-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59995-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="59995-135">-NextLink</span></span>
<span data-ttu-id="59995-136">Sonraki bağlantıyı belirtir.</span><span class="sxs-lookup"><span data-stu-id="59995-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59995-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59995-137">-ResourceGroupName</span></span>
<span data-ttu-id="59995-138">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59995-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59995-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="59995-139">-Status</span></span>
<span data-ttu-id="59995-140">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59995-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59995-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59995-141">CommonParameters</span></span>
<span data-ttu-id="59995-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59995-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59995-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59995-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59995-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59995-144">INPUTS</span></span>

### <span data-ttu-id="59995-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59995-145">None</span></span>
<span data-ttu-id="59995-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="59995-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59995-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59995-147">OUTPUTS</span></span>

### <span data-ttu-id="59995-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="59995-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="59995-149">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="59995-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="59995-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59995-150">NOTES</span></span>

## <span data-ttu-id="59995-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59995-151">RELATED LINKS</span></span>

[<span data-ttu-id="59995-152">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="59995-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="59995-153">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="59995-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="59995-154">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="59995-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="59995-155">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="59995-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="59995-156">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="59995-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="59995-157">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="59995-157">Update-AzVM</span></span>](./Update-AzVM.md)


