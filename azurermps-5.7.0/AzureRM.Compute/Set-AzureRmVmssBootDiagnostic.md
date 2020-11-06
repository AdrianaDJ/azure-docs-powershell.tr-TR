---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591048"
---
# <span data-ttu-id="473dd-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="473dd-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="473dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="473dd-102">SYNOPSIS</span></span>
<span data-ttu-id="473dd-103">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="473dd-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="473dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="473dd-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="473dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="473dd-105">DESCRIPTION</span></span>
<span data-ttu-id="473dd-106">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="473dd-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="473dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="473dd-107">EXAMPLES</span></span>

### <span data-ttu-id="473dd-108">Örnek 1: bir VMSS için önyükleme tanılama profili özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="473dd-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="473dd-109">Bu komut, ContosoVMSS adlı VMSS için önyükleme tanılama profili özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="473dd-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="473dd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="473dd-110">PARAMETERS</span></span>

### <span data-ttu-id="473dd-111">Özellikli</span><span class="sxs-lookup"><span data-stu-id="473dd-111">-Enabled</span></span>
<span data-ttu-id="473dd-112">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="473dd-112">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="473dd-113">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="473dd-113">-StorageUri</span></span>
<span data-ttu-id="473dd-114">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="473dd-114">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="473dd-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="473dd-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="473dd-116">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="473dd-116">Specifies the VMSS object.</span></span>
<span data-ttu-id="473dd-117">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="473dd-117">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="473dd-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="473dd-118">-Confirm</span></span>
<span data-ttu-id="473dd-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="473dd-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473dd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="473dd-120">-WhatIf</span></span>
<span data-ttu-id="473dd-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="473dd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="473dd-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="473dd-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473dd-123">CommonParameters</span></span>
<span data-ttu-id="473dd-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="473dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473dd-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473dd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473dd-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="473dd-126">INPUTS</span></span>

### <span data-ttu-id="473dd-127">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="473dd-127">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="473dd-128">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="473dd-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="473dd-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="473dd-129">OUTPUTS</span></span>

### <span data-ttu-id="473dd-130">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="473dd-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="473dd-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="473dd-131">NOTES</span></span>

## <span data-ttu-id="473dd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="473dd-132">RELATED LINKS</span></span>

