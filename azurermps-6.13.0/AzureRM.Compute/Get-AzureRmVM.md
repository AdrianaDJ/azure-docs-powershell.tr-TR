---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588555"
---
# <span data-ttu-id="6992e-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6992e-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="6992e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6992e-102">SYNOPSIS</span></span>
<span data-ttu-id="6992e-103">Sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6992e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6992e-104">SYNTAX</span></span>

### <span data-ttu-id="6992e-105">Listallvirtual, Inesparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6992e-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6992e-106">Listvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="6992e-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6992e-107">Getvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="6992e-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6992e-108">Listlocationvirtual</span><span class="sxs-lookup"><span data-stu-id="6992e-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6992e-109">Listnextlinkvirtual, Inesparamset</span><span class="sxs-lookup"><span data-stu-id="6992e-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6992e-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="6992e-110">DESCRIPTION</span></span>
<span data-ttu-id="6992e-111">**Get-AzureRmVM** cmdlet 'i, bir Azure sanal makinesinin model görünümünü ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="6992e-112">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="6992e-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="6992e-113">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="6992e-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="6992e-114">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6992e-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="6992e-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6992e-115">EXAMPLES</span></span>

### <span data-ttu-id="6992e-116">Örnek 1: model ve örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6992e-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="6992e-117">Bu komut, VirtualMachine07 adındaki sanal makinenin model görünümü ve örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="6992e-118">Örnek 2: örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6992e-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="6992e-119">Bu komut, VirtualMachine07 adındaki sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="6992e-120">Bu komut, *Status* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6992e-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="6992e-121">Bu nedenle, komut yalnızca örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="6992e-122">Örnek 3: kaynak grubundaki tüm sanal makinelerin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6992e-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="6992e-123">Bu komut, ResourceGroup11 adlı kaynak grubundaki tüm sanal makinelerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="6992e-124">Örnek 4: aboneliğinizdeki tüm sanal makineleri edinme</span><span class="sxs-lookup"><span data-stu-id="6992e-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="6992e-125">Bu komut aboneliğinizdeki tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="6992e-126">Örnek 5: konumdaki tüm sanal makineleri edinin.</span><span class="sxs-lookup"><span data-stu-id="6992e-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="6992e-127">Bu komut, Batı ABD bölgesindeki tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="6992e-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="6992e-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6992e-128">PARAMETERS</span></span>

### <span data-ttu-id="6992e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6992e-129">-DefaultProfile</span></span>
<span data-ttu-id="6992e-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6992e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6992e-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="6992e-131">-DisplayHint</span></span>
<span data-ttu-id="6992e-132">Sanal makine nesnesinin nasıl görüntülendiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="6992e-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="6992e-133">Geçerli değerler:--Compact: yalnızca üst düzey özelliklerini görüntüler--Genişlet: tüm düzeylerdeki tüm özellikleri görüntüler</span><span class="sxs-lookup"><span data-stu-id="6992e-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6992e-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="6992e-134">-Location</span></span>
<span data-ttu-id="6992e-135">Görüntülenecek sanal makinelerin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6992e-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6992e-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="6992e-136">-Name</span></span>
<span data-ttu-id="6992e-137">Alınacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6992e-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6992e-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="6992e-138">-NextLink</span></span>
<span data-ttu-id="6992e-139">Sonraki bağlantıyı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6992e-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6992e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6992e-140">-ResourceGroupName</span></span>
<span data-ttu-id="6992e-141">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6992e-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6992e-142">-Durum</span><span class="sxs-lookup"><span data-stu-id="6992e-142">-Status</span></span>
<span data-ttu-id="6992e-143">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6992e-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6992e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6992e-144">CommonParameters</span></span>
<span data-ttu-id="6992e-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6992e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6992e-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6992e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6992e-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6992e-147">INPUTS</span></span>

### <span data-ttu-id="6992e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6992e-148">System.String</span></span>

### <span data-ttu-id="6992e-149">System. Uri</span><span class="sxs-lookup"><span data-stu-id="6992e-149">System.Uri</span></span>

### <span data-ttu-id="6992e-150">Microsoft. Azure. Commands. COMPUTE. modeller. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="6992e-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="6992e-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6992e-151">OUTPUTS</span></span>

### <span data-ttu-id="6992e-152">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6992e-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6992e-153">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="6992e-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="6992e-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6992e-154">NOTES</span></span>

## <span data-ttu-id="6992e-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6992e-155">RELATED LINKS</span></span>

[<span data-ttu-id="6992e-156">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6992e-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="6992e-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6992e-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="6992e-158">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6992e-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="6992e-159">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6992e-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="6992e-160">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6992e-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="6992e-161">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6992e-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


