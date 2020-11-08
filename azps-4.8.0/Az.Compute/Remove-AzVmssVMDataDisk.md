---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109101"
---
# <span data-ttu-id="ec82a-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ec82a-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="ec82a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec82a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec82a-103">Sanal makine ölçek kümesi VM 'den veri diskini kaldırır</span><span class="sxs-lookup"><span data-stu-id="ec82a-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="ec82a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec82a-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec82a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec82a-105">DESCRIPTION</span></span>
<span data-ttu-id="ec82a-106">**Remove-Azvmssvmdatadısk** CMDLET 'i VM Ölçek kümesi VM 'den veri diskini kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="ec82a-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="ec82a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec82a-107">EXAMPLES</span></span>

### <span data-ttu-id="ec82a-108">Örnek 1: VM Ölçek kümesi VM 'den veri diskini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ec82a-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="ec82a-109">İlk komut getsan mevcut VMSS VM 'si kaynak grubu adı, VMSS adı ve örnek KIMLIĞI tarafından verilir.</span><span class="sxs-lookup"><span data-stu-id="ec82a-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="ec82a-110">İkinci komut, 0 veri diski LUN değerini, VM Ölçek kümesi $VmssVM VM 'den (son komutu</span><span class="sxs-lookup"><span data-stu-id="ec82a-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="ec82a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec82a-111">PARAMETERS</span></span>

### <span data-ttu-id="ec82a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec82a-112">-DefaultProfile</span></span>
<span data-ttu-id="ec82a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec82a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec82a-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="ec82a-114">-Lun</span></span>
<span data-ttu-id="ec82a-115">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec82a-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="ec82a-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="ec82a-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="ec82a-117">Sanal makine ölçeği kümesi VM profili.</span><span class="sxs-lookup"><span data-stu-id="ec82a-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec82a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec82a-118">CommonParameters</span></span>
<span data-ttu-id="ec82a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec82a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec82a-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec82a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec82a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec82a-121">INPUTS</span></span>

### <span data-ttu-id="ec82a-122">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="ec82a-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="ec82a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec82a-123">OUTPUTS</span></span>

### <span data-ttu-id="ec82a-124">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="ec82a-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="ec82a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec82a-125">NOTES</span></span>

## <span data-ttu-id="ec82a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec82a-126">RELATED LINKS</span></span>
