---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: afe5c168c9a5f3633ce4766df5938a81ccc60510
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762279"
---
# <span data-ttu-id="5d23b-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d23b-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="5d23b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d23b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d23b-103">Sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d23b-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d23b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d23b-104">SYNTAX</span></span>

### <span data-ttu-id="5d23b-105">Listallvirtual, Inesparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d23b-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d23b-106">Listvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="5d23b-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d23b-107">Getvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="5d23b-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d23b-108">Listnextlinkvirtual, Inesparamset</span><span class="sxs-lookup"><span data-stu-id="5d23b-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d23b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d23b-109">DESCRIPTION</span></span>
<span data-ttu-id="5d23b-110">**Get-AzureRmVM** cmdlet 'i, bir Azure sanal makinesinin model görünümünü ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="5d23b-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="5d23b-111">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="5d23b-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="5d23b-112">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="5d23b-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="5d23b-113">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5d23b-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="5d23b-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d23b-114">EXAMPLES</span></span>

### <span data-ttu-id="5d23b-115">Örnek 1: model ve örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="5d23b-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="5d23b-116">Bu komut, VirtualMachine07 adındaki sanal makinenin model görünümü ve örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d23b-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="5d23b-117">Örnek 2: örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="5d23b-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="5d23b-118">Bu komut, VirtualMachine07 adındaki sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d23b-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="5d23b-119">Bu komut, *Status* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d23b-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="5d23b-120">Bu nedenle, komut yalnızca örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d23b-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="5d23b-121">Örnek 3: kaynak grubundaki tüm sanal makinelerin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="5d23b-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5d23b-122">Bu komut, ResourceGroup11 adlı kaynak grubundaki tüm sanal makinelerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d23b-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="5d23b-123">Örnek 4: aboneliğinizdeki tüm sanal makineleri edinme</span><span class="sxs-lookup"><span data-stu-id="5d23b-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="5d23b-124">Bu komut aboneliğinizdeki tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="5d23b-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="5d23b-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d23b-125">PARAMETERS</span></span>

### <span data-ttu-id="5d23b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d23b-126">-DefaultProfile</span></span>
<span data-ttu-id="5d23b-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d23b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d23b-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="5d23b-128">-DisplayHint</span></span>
<span data-ttu-id="5d23b-129">Sanal makine nesnesinin nasıl görüntülendiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="5d23b-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="5d23b-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="5d23b-130">Valid values are:</span></span>

<span data-ttu-id="5d23b-131">--Compact: yalnızca üst düzey özelliklerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="5d23b-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="5d23b-132">--Genişlet: tüm düzeylerdeki tüm özellikleri görüntüler</span><span class="sxs-lookup"><span data-stu-id="5d23b-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="5d23b-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d23b-133">-Name</span></span>
<span data-ttu-id="5d23b-134">Alınacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d23b-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="5d23b-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="5d23b-135">-NextLink</span></span>
<span data-ttu-id="5d23b-136">Sonraki bağlantıyı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d23b-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="5d23b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d23b-137">-ResourceGroupName</span></span>
<span data-ttu-id="5d23b-138">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d23b-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5d23b-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="5d23b-139">-Status</span></span>
<span data-ttu-id="5d23b-140">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d23b-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="5d23b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d23b-141">CommonParameters</span></span>
<span data-ttu-id="5d23b-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d23b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d23b-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d23b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d23b-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d23b-144">INPUTS</span></span>

## <span data-ttu-id="5d23b-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d23b-145">OUTPUTS</span></span>

## <span data-ttu-id="5d23b-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d23b-146">NOTES</span></span>

## <span data-ttu-id="5d23b-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d23b-147">RELATED LINKS</span></span>

[<span data-ttu-id="5d23b-148">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d23b-148">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="5d23b-149">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d23b-149">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5d23b-150">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d23b-150">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="5d23b-151">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d23b-151">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5d23b-152">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d23b-152">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="5d23b-153">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d23b-153">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


