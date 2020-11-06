---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: dcfc0fcf2901f7f604e4d39e330db61633ef0dee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586921"
---
# <span data-ttu-id="4d5c9-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4d5c9-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="4d5c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d5c9-103">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d5c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d5c9-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d5c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="4d5c9-106">Sanal makine ölçek kümesi önyükleme tanılaması profilini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="4d5c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d5c9-107">EXAMPLES</span></span>

### <span data-ttu-id="4d5c9-108">Örnek 1: bir VMSS için önyükleme tanılama profili özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4d5c9-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="4d5c9-109">Bu komut, ContosoVMSS adlı VMSS için önyükleme tanılama profili özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4d5c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d5c9-110">PARAMETERS</span></span>

### <span data-ttu-id="4d5c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d5c9-111">-DefaultProfile</span></span>
<span data-ttu-id="4d5c9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d5c9-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="4d5c9-113">-Enabled</span></span>
<span data-ttu-id="4d5c9-114">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4d5c9-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="4d5c9-115">-StorageUri</span></span>
<span data-ttu-id="4d5c9-116">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="4d5c9-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d5c9-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4d5c9-118">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="4d5c9-119">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4d5c9-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d5c9-120">-Confirm</span></span>
<span data-ttu-id="4d5c9-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d5c9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d5c9-122">-WhatIf</span></span>
<span data-ttu-id="4d5c9-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d5c9-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d5c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d5c9-125">CommonParameters</span></span>
<span data-ttu-id="4d5c9-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d5c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d5c9-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d5c9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d5c9-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d5c9-128">INPUTS</span></span>

### <span data-ttu-id="4d5c9-129">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d5c9-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="4d5c9-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="4d5c9-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="4d5c9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d5c9-131">OUTPUTS</span></span>

### <span data-ttu-id="4d5c9-132">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d5c9-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="4d5c9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d5c9-133">NOTES</span></span>

## <span data-ttu-id="4d5c9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d5c9-134">RELATED LINKS</span></span>

