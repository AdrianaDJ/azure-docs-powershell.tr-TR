---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b3e9f8703b2130426d98a4a59fe25eb2f3f8fbdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586797"
---
# <span data-ttu-id="24df4-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="24df4-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="24df4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24df4-102">SYNOPSIS</span></span>
<span data-ttu-id="24df4-103">Bir kaynak grubundaki sanal makineden DSC genişletme işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24df4-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24df4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24df4-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24df4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24df4-105">DESCRIPTION</span></span>
<span data-ttu-id="24df4-106">**Remove-AzureRmVMDscExtension** cmdlet 'i, bir kaynak grubundaki sanal makineden Istenen durum yapılandırma (DSC) uzantı işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24df4-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="24df4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24df4-107">EXAMPLES</span></span>

### <span data-ttu-id="24df4-108">Örnek 1: DSC uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="24df4-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResouceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="24df4-109">Bu komut, VM07 adındaki sanal makinede DSC adlı uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24df4-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="24df4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24df4-110">PARAMETERS</span></span>

### <span data-ttu-id="24df4-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="24df4-111">-Name</span></span>
<span data-ttu-id="24df4-112">Bu cmdlet 'in kaldırıldığı DSC uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24df4-112">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="24df4-113">Set-AzureRmVMDscExtension cmdlet, **Remove-AzureRmVMDscExtension** tarafından kullanılan varsayılan değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="24df4-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="24df4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24df4-114">-ResourceGroupName</span></span>
<span data-ttu-id="24df4-115">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24df4-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="24df4-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="24df4-116">-VMName</span></span>
<span data-ttu-id="24df4-117">Bu cmdlet 'in DSC uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24df4-117">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="24df4-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="24df4-118">-Confirm</span></span>
<span data-ttu-id="24df4-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24df4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24df4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24df4-120">-WhatIf</span></span>
<span data-ttu-id="24df4-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24df4-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="24df4-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24df4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24df4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24df4-123">CommonParameters</span></span>
<span data-ttu-id="24df4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24df4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24df4-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24df4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24df4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24df4-126">INPUTS</span></span>

### <span data-ttu-id="24df4-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="24df4-127">None</span></span>
<span data-ttu-id="24df4-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="24df4-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24df4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24df4-129">OUTPUTS</span></span>

## <span data-ttu-id="24df4-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24df4-130">NOTES</span></span>

## <span data-ttu-id="24df4-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24df4-131">RELATED LINKS</span></span>

[<span data-ttu-id="24df4-132">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="24df4-132">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="24df4-133">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="24df4-133">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


