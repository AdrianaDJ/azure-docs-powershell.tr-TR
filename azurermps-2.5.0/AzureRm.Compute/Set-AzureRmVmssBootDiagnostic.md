---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
ms.openlocfilehash: cca99d994380483465f9026ba8023cd92afc7e37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938884"
---
# <span data-ttu-id="b1357-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b1357-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="b1357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1357-102">SYNOPSIS</span></span>
<span data-ttu-id="b1357-103">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b1357-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1357-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1357-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1357-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1357-105">DESCRIPTION</span></span>
<span data-ttu-id="b1357-106">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b1357-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="b1357-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1357-107">EXAMPLES</span></span>

### <span data-ttu-id="b1357-108">Örnek 1: bir VMSS için önyükleme tanılama profili özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b1357-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="b1357-109">Bu komut, ContosoVMSS adlı VMSS için önyükleme tanılama profili özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b1357-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="b1357-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1357-110">PARAMETERS</span></span>

### <span data-ttu-id="b1357-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1357-111">-DefaultProfile</span></span>
<span data-ttu-id="b1357-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1357-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1357-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="b1357-113">-Enabled</span></span>
<span data-ttu-id="b1357-114">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="b1357-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b1357-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b1357-115">-StorageUri</span></span>
<span data-ttu-id="b1357-116">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="b1357-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="b1357-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b1357-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b1357-118">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1357-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="b1357-119">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1357-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="b1357-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1357-120">-Confirm</span></span>
<span data-ttu-id="b1357-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1357-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1357-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1357-122">-WhatIf</span></span>
<span data-ttu-id="b1357-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1357-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1357-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1357-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1357-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1357-125">CommonParameters</span></span>
<span data-ttu-id="b1357-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1357-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1357-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1357-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1357-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1357-128">INPUTS</span></span>

### <span data-ttu-id="b1357-129">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b1357-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="b1357-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="b1357-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="b1357-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1357-131">OUTPUTS</span></span>

### <span data-ttu-id="b1357-132">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b1357-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="b1357-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1357-133">NOTES</span></span>

## <span data-ttu-id="b1357-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1357-134">RELATED LINKS</span></span>

