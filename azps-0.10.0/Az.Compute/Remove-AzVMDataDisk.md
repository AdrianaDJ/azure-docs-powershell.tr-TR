---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 3529ca1d26504558036f3496c9bc75ec10e666ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936910"
---
# <span data-ttu-id="8cb21-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8cb21-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="8cb21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cb21-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb21-103">Sanal makineden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8cb21-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="8cb21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8cb21-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cb21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8cb21-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb21-106">**Remove-Azvmdatadısk** cmdlet 'i, bir sanal makineden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8cb21-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="8cb21-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8cb21-107">EXAMPLES</span></span>

### <span data-ttu-id="8cb21-108">Örnek 1: sanal makineden veri diskini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8cb21-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="8cb21-109">İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzVM** cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="8cb21-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="8cb21-110">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="8cb21-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8cb21-111">İkinci komut, $VirtualMachine depolanan sanal makineden disk3 adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8cb21-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="8cb21-112">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8cb21-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="8cb21-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8cb21-113">PARAMETERS</span></span>

### <span data-ttu-id="8cb21-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="8cb21-114">-DataDiskNames</span></span>
<span data-ttu-id="8cb21-115">Bu cmdlet 'in kaldırdığı bir veya birden çok veri diskine ait adları belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cb21-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb21-116">-DefaultProfile</span></span>
<span data-ttu-id="8cb21-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8cb21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cb21-118">-VM</span><span class="sxs-lookup"><span data-stu-id="8cb21-118">-VM</span></span>
<span data-ttu-id="8cb21-119">Veri diskinin kaldırılacağı yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cb21-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="8cb21-120">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8cb21-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb21-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="8cb21-121">-Confirm</span></span>
<span data-ttu-id="8cb21-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8cb21-122">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb21-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb21-123">-WhatIf</span></span>
<span data-ttu-id="8cb21-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8cb21-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cb21-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8cb21-125">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb21-126">CommonParameters</span></span>
<span data-ttu-id="8cb21-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8cb21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb21-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb21-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb21-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8cb21-129">INPUTS</span></span>

### <span data-ttu-id="8cb21-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8cb21-130">PSVirtualMachine</span></span>
<span data-ttu-id="8cb21-131">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8cb21-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="8cb21-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8cb21-132">OUTPUTS</span></span>

### <span data-ttu-id="8cb21-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8cb21-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8cb21-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8cb21-134">NOTES</span></span>

## <span data-ttu-id="8cb21-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8cb21-135">RELATED LINKS</span></span>

[<span data-ttu-id="8cb21-136">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8cb21-136">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="8cb21-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8cb21-137">Get-AzVM</span></span>](./Get-AzVM.md)


