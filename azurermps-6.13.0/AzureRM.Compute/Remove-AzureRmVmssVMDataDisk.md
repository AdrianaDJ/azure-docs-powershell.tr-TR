---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: 5c82c2dfb852cd6c3d397b34e90d9a611ff0efaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594438"
---
# <span data-ttu-id="502dc-101">Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="502dc-101">Remove-AzureRmVmssVMDataDisk</span></span>

## <span data-ttu-id="502dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="502dc-102">SYNOPSIS</span></span>
<span data-ttu-id="502dc-103">Sanal makine ölçek kümesi VM 'den veri diskini kaldırır</span><span class="sxs-lookup"><span data-stu-id="502dc-103">Removes a data disk from a virtual machine scale set VM</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="502dc-104">SYNTAX</span></span>

```
Remove-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="502dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="502dc-105">DESCRIPTION</span></span>
<span data-ttu-id="502dc-106">**Remove-Azurermvmssvmdatadısk** CMDLET 'i VM Ölçek kümesi VM 'den veri diskini kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="502dc-106">The **Remove-AzureRmVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="502dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="502dc-107">EXAMPLES</span></span>

### <span data-ttu-id="502dc-108">Örnek 1: VM Ölçek kümesi VM 'den veri diskini kaldırma</span><span class="sxs-lookup"><span data-stu-id="502dc-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzureRmVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="502dc-109">İlk komut getsan mevcut VMSS VM 'si kaynak grubu adı, VMSS adı ve örnek KIMLIĞI tarafından verilir.</span><span class="sxs-lookup"><span data-stu-id="502dc-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="502dc-110">İkinci komut, 0 veri diski LUN değerini, VM Ölçek kümesi $VmssVM VM 'den (son komutu</span><span class="sxs-lookup"><span data-stu-id="502dc-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="502dc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="502dc-111">PARAMETERS</span></span>

### <span data-ttu-id="502dc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502dc-112">-DefaultProfile</span></span>
<span data-ttu-id="502dc-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="502dc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="502dc-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="502dc-114">-Lun</span></span>
<span data-ttu-id="502dc-115">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="502dc-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502dc-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="502dc-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="502dc-117">Sanal makine ölçeği kümesi VM profili.</span><span class="sxs-lookup"><span data-stu-id="502dc-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="502dc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502dc-118">CommonParameters</span></span>
<span data-ttu-id="502dc-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="502dc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502dc-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502dc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502dc-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="502dc-121">INPUTS</span></span>

### <span data-ttu-id="502dc-122">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="502dc-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="502dc-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="502dc-123">OUTPUTS</span></span>

### <span data-ttu-id="502dc-124">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="502dc-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="502dc-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="502dc-125">NOTES</span></span>

## <span data-ttu-id="502dc-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="502dc-126">RELATED LINKS</span></span>
