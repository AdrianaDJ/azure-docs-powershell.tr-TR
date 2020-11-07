---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 482398d3ba0934f17b1381edc5dac08fb22bd75a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936813"
---
# <span data-ttu-id="d8242-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8242-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="d8242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8242-102">SYNOPSIS</span></span>
<span data-ttu-id="d8242-103">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8242-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d8242-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8242-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8242-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8242-105">DESCRIPTION</span></span>
<span data-ttu-id="d8242-106">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8242-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d8242-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8242-107">EXAMPLES</span></span>

### <span data-ttu-id="d8242-108">Örnek 1: bir VMSS için önyükleme tanılama profili özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d8242-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="d8242-109">Bu komut, ContosoVMSS adlı VMSS için önyükleme tanılama profili özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8242-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d8242-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8242-110">PARAMETERS</span></span>

### <span data-ttu-id="d8242-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8242-111">-DefaultProfile</span></span>
<span data-ttu-id="d8242-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8242-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8242-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="d8242-113">-Enabled</span></span>
<span data-ttu-id="d8242-114">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="d8242-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d8242-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d8242-115">-StorageUri</span></span>
<span data-ttu-id="d8242-116">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="d8242-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="d8242-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d8242-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d8242-118">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8242-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="d8242-119">Nesneyi oluşturmak için New-AzVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8242-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8242-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8242-120">-Confirm</span></span>
<span data-ttu-id="d8242-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8242-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8242-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8242-122">-WhatIf</span></span>
<span data-ttu-id="d8242-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8242-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8242-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8242-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8242-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8242-125">CommonParameters</span></span>
<span data-ttu-id="d8242-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8242-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8242-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8242-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8242-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8242-128">INPUTS</span></span>

### <span data-ttu-id="d8242-129">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d8242-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="d8242-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="d8242-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="d8242-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8242-131">OUTPUTS</span></span>

### <span data-ttu-id="d8242-132">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d8242-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="d8242-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8242-133">NOTES</span></span>

## <span data-ttu-id="d8242-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8242-134">RELATED LINKS</span></span>

