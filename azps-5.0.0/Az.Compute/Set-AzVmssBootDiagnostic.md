---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319658"
---
# <span data-ttu-id="e6633-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e6633-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="e6633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6633-102">SYNOPSIS</span></span>
<span data-ttu-id="e6633-103">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6633-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="e6633-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6633-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6633-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6633-105">DESCRIPTION</span></span>
<span data-ttu-id="e6633-106">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6633-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="e6633-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6633-107">EXAMPLES</span></span>

### <span data-ttu-id="e6633-108">Örnek 1: bir VMSS için önyükleme tanılama profili özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e6633-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="e6633-109">Bu komut, ContosoVMSS adlı VMSS için önyükleme tanılama profili özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6633-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="e6633-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6633-110">PARAMETERS</span></span>

### <span data-ttu-id="e6633-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6633-111">-DefaultProfile</span></span>
<span data-ttu-id="e6633-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6633-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6633-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="e6633-113">-Enabled</span></span>
<span data-ttu-id="e6633-114">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="e6633-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6633-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="e6633-115">-StorageUri</span></span>
<span data-ttu-id="e6633-116">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="e6633-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6633-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e6633-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e6633-118">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6633-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="e6633-119">Nesneyi oluşturmak için New-AzVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6633-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6633-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6633-120">-Confirm</span></span>
<span data-ttu-id="e6633-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6633-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6633-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6633-122">-WhatIf</span></span>
<span data-ttu-id="e6633-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6633-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6633-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6633-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6633-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6633-125">CommonParameters</span></span>
<span data-ttu-id="e6633-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6633-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6633-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e6633-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6633-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6633-128">INPUTS</span></span>

### <span data-ttu-id="e6633-129">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e6633-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e6633-130">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6633-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e6633-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e6633-131">System.String</span></span>

## <span data-ttu-id="e6633-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6633-132">OUTPUTS</span></span>

### <span data-ttu-id="e6633-133">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e6633-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e6633-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6633-134">NOTES</span></span>

## <span data-ttu-id="e6633-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6633-135">RELATED LINKS</span></span>
