---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4dbae539d43961d954dba6ea12bd88e08d9616ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591065"
---
# <span data-ttu-id="42ef0-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="42ef0-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="42ef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="42ef0-103">Bir Azure Resource Manager (ARM) sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="42ef0-103">Gets the properties of an Azure Resource Manager (ARM) virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ef0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42ef0-104">SYNTAX</span></span>

### <span data-ttu-id="42ef0-105">Listallvirtual, Inesparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42ef0-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ef0-106">Listvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="42ef0-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42ef0-107">Getvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="42ef0-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ef0-108">Listnextlinkvirtual, Inesparamset</span><span class="sxs-lookup"><span data-stu-id="42ef0-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42ef0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="42ef0-109">DESCRIPTION</span></span>
<span data-ttu-id="42ef0-110">**Get-AzureRmVM** cmdlet 'i, bir Azure sanal makinesinin model görünümünü ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="42ef0-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="42ef0-111">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="42ef0-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="42ef0-112">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="42ef0-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="42ef0-113">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="42ef0-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="42ef0-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42ef0-114">EXAMPLES</span></span>

### <span data-ttu-id="42ef0-115">Örnek 1: model ve örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="42ef0-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="42ef0-116">Bu komut, VirtualMachine07 adındaki sanal makinenin model görünümü ve örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="42ef0-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="42ef0-117">Örnek 2: örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="42ef0-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="42ef0-118">Bu komut, VirtualMachine07 adındaki sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="42ef0-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="42ef0-119">Bu komut, *Status* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42ef0-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="42ef0-120">Bu nedenle, komut yalnızca örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="42ef0-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="42ef0-121">Örnek 3: kaynak grubundaki tüm sanal makinelerin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="42ef0-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="42ef0-122">Bu komut, ResourceGroup11 adlı kaynak grubundaki tüm sanal makinelerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="42ef0-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="42ef0-123">Örnek 4: aboneliğinizdeki tüm sanal makineleri edinme</span><span class="sxs-lookup"><span data-stu-id="42ef0-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="42ef0-124">Bu komut aboneliğinizdeki tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="42ef0-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="42ef0-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42ef0-125">PARAMETERS</span></span>

### <span data-ttu-id="42ef0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ef0-126">-DefaultProfile</span></span>
<span data-ttu-id="42ef0-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42ef0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42ef0-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="42ef0-128">-DisplayHint</span></span>
<span data-ttu-id="42ef0-129">Sanal makine nesnesinin nasıl görüntülendiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="42ef0-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="42ef0-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="42ef0-130">Valid values are:</span></span>

<span data-ttu-id="42ef0-131">--Compact: yalnızca üst düzey özelliklerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="42ef0-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="42ef0-132">--Genişlet: tüm düzeylerdeki tüm özellikleri görüntüler</span><span class="sxs-lookup"><span data-stu-id="42ef0-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="42ef0-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="42ef0-133">-Name</span></span>
<span data-ttu-id="42ef0-134">Alınacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42ef0-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="42ef0-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="42ef0-135">-NextLink</span></span>
<span data-ttu-id="42ef0-136">Sonraki bağlantıyı belirtir.</span><span class="sxs-lookup"><span data-stu-id="42ef0-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="42ef0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42ef0-137">-ResourceGroupName</span></span>
<span data-ttu-id="42ef0-138">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42ef0-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="42ef0-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="42ef0-139">-Status</span></span>
<span data-ttu-id="42ef0-140">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42ef0-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="42ef0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ef0-141">CommonParameters</span></span>
<span data-ttu-id="42ef0-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42ef0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ef0-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ef0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ef0-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42ef0-144">INPUTS</span></span>

### <span data-ttu-id="42ef0-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="42ef0-145">None</span></span>
<span data-ttu-id="42ef0-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="42ef0-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42ef0-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42ef0-147">OUTPUTS</span></span>

### <span data-ttu-id="42ef0-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="42ef0-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="42ef0-149">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="42ef0-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="42ef0-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42ef0-150">NOTES</span></span>

## <span data-ttu-id="42ef0-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42ef0-151">RELATED LINKS</span></span>

[<span data-ttu-id="42ef0-152">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="42ef0-152">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="42ef0-153">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="42ef0-153">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="42ef0-154">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="42ef0-154">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="42ef0-155">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="42ef0-155">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="42ef0-156">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="42ef0-156">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="42ef0-157">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="42ef0-157">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


