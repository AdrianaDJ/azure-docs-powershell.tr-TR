---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 2fdbafba325d95f8e0ce2959e6f77c896dfa0722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752771"
---
# <span data-ttu-id="dbb6a-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dbb6a-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="dbb6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb6a-103">Bir kaynak grubundaki sanal makineden DSC genişletme işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="dbb6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbb6a-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbb6a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="dbb6a-106">**Remove-AzVMDscExtension** cmdlet 'i, bir kaynak grubundaki sanal makineden Istenen durum yapılandırma (DSC) uzantı işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="dbb6a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbb6a-107">EXAMPLES</span></span>

### <span data-ttu-id="dbb6a-108">Örnek 1: DSC uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="dbb6a-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="dbb6a-109">Bu komut, VM07 adındaki sanal makinede DSC adlı uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="dbb6a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbb6a-110">PARAMETERS</span></span>

### <span data-ttu-id="dbb6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb6a-111">-DefaultProfile</span></span>
<span data-ttu-id="dbb6a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbb6a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbb6a-113">-Name</span></span>
<span data-ttu-id="dbb6a-114">Bu cmdlet 'in kaldırıldığı DSC uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="dbb6a-115">Set-AzVMDscExtension cmdlet 'i, **Remove-AzVMDscExtension** tarafından kullanılan varsayılan değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="dbb6a-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dbb6a-116">-NoWait</span></span>
<span data-ttu-id="dbb6a-117">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="dbb6a-118">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbb6a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbb6a-119">-ResourceGroupName</span></span>
<span data-ttu-id="dbb6a-120">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbb6a-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="dbb6a-121">-VMName</span></span>
<span data-ttu-id="dbb6a-122">Bu cmdlet 'in DSC uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbb6a-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbb6a-123">-Confirm</span></span>
<span data-ttu-id="dbb6a-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbb6a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbb6a-125">-WhatIf</span></span>
<span data-ttu-id="dbb6a-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbb6a-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbb6a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb6a-128">CommonParameters</span></span>
<span data-ttu-id="dbb6a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb6a-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dbb6a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb6a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbb6a-131">INPUTS</span></span>

### <span data-ttu-id="dbb6a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dbb6a-132">System.String</span></span>

## <span data-ttu-id="dbb6a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbb6a-133">OUTPUTS</span></span>

### <span data-ttu-id="dbb6a-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dbb6a-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dbb6a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbb6a-135">NOTES</span></span>

## <span data-ttu-id="dbb6a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbb6a-136">RELATED LINKS</span></span>

[<span data-ttu-id="dbb6a-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dbb6a-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="dbb6a-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dbb6a-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


