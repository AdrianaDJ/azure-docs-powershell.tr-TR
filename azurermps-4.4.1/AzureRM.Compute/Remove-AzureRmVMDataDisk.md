---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 774166f88e4ca94e5e21c2b96817596c082a429c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586973"
---
# <span data-ttu-id="6a6d2-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6a6d2-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="6a6d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6d2-103">Sanal makineden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a6d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a6d2-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a6d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a6d2-105">DESCRIPTION</span></span>
<span data-ttu-id="6a6d2-106">**Remove-Azurermvmdatadısk** cmdlet 'i, bir sanal makineden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="6a6d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a6d2-107">EXAMPLES</span></span>

### <span data-ttu-id="6a6d2-108">Örnek 1: sanal makineden veri diskini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6a6d2-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6a6d2-109">İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzureRmVM** cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="6a6d2-110">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="6a6d2-111">İkinci komut, $VirtualMachine depolanan sanal makineden disk3 adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="6a6d2-112">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="6a6d2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a6d2-113">PARAMETERS</span></span>

### <span data-ttu-id="6a6d2-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="6a6d2-114">-DataDiskNames</span></span>
<span data-ttu-id="6a6d2-115">Bu cmdlet 'in kaldırdığı bir veya birden çok veri diskine ait adları belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6d2-116">-DefaultProfile</span></span>
<span data-ttu-id="6a6d2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a6d2-118">-VM</span><span class="sxs-lookup"><span data-stu-id="6a6d2-118">-VM</span></span>
<span data-ttu-id="6a6d2-119">Veri diskinin kaldırılacağı yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="6a6d2-120">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a6d2-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a6d2-121">-Confirm</span></span>
<span data-ttu-id="6a6d2-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-122">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a6d2-123">-WhatIf</span></span>
<span data-ttu-id="6a6d2-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a6d2-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-125">The cmdlet is not run.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6d2-126">CommonParameters</span></span>
<span data-ttu-id="6a6d2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6d2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a6d2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6d2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a6d2-129">INPUTS</span></span>

## <span data-ttu-id="6a6d2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a6d2-130">OUTPUTS</span></span>

## <span data-ttu-id="6a6d2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a6d2-131">NOTES</span></span>

## <span data-ttu-id="6a6d2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a6d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a6d2-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6a6d2-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="6a6d2-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6a6d2-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


