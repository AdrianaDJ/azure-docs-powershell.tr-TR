---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 69eff38068c379dadc4f3a061cfba4f9cb6539e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936907"
---
# <span data-ttu-id="00cfb-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="00cfb-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="00cfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="00cfb-103">Bir kaynak grubundaki sanal makineden DSC genişletme işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00cfb-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="00cfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00cfb-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00cfb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="00cfb-106">**Remove-AzVMDscExtension** cmdlet 'i, bir kaynak grubundaki sanal makineden Istenen durum yapılandırma (DSC) uzantı işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00cfb-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="00cfb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00cfb-107">EXAMPLES</span></span>

### <span data-ttu-id="00cfb-108">Örnek 1: DSC uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="00cfb-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="00cfb-109">Bu komut, VM07 adındaki sanal makinede DSC adlı uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00cfb-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="00cfb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00cfb-110">PARAMETERS</span></span>

### <span data-ttu-id="00cfb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00cfb-111">-DefaultProfile</span></span>
<span data-ttu-id="00cfb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00cfb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00cfb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="00cfb-113">-Name</span></span>
<span data-ttu-id="00cfb-114">Bu cmdlet 'in kaldırıldığı DSC uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00cfb-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="00cfb-115">Set-AzVMDscExtension cmdlet 'i, **Remove-AzVMDscExtension** tarafından kullanılan varsayılan değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="00cfb-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="00cfb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00cfb-116">-ResourceGroupName</span></span>
<span data-ttu-id="00cfb-117">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00cfb-117">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00cfb-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="00cfb-118">-VMName</span></span>
<span data-ttu-id="00cfb-119">Bu cmdlet 'in DSC uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00cfb-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00cfb-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="00cfb-120">-Confirm</span></span>
<span data-ttu-id="00cfb-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00cfb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00cfb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00cfb-122">-WhatIf</span></span>
<span data-ttu-id="00cfb-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00cfb-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="00cfb-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00cfb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00cfb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00cfb-125">CommonParameters</span></span>
<span data-ttu-id="00cfb-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00cfb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00cfb-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00cfb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00cfb-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00cfb-128">INPUTS</span></span>

### <span data-ttu-id="00cfb-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="00cfb-129">None</span></span>
<span data-ttu-id="00cfb-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="00cfb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00cfb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00cfb-131">OUTPUTS</span></span>

### <span data-ttu-id="00cfb-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="00cfb-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="00cfb-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00cfb-133">NOTES</span></span>

## <span data-ttu-id="00cfb-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00cfb-134">RELATED LINKS</span></span>

[<span data-ttu-id="00cfb-135">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="00cfb-135">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="00cfb-136">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="00cfb-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)

