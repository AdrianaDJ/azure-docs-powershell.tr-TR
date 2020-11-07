---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936886"
---
# <span data-ttu-id="595ae-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="595ae-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="595ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595ae-102">SYNOPSIS</span></span>
<span data-ttu-id="595ae-103">Bir uzantıyı VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="595ae-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="595ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="595ae-104">SYNTAX</span></span>

### <span data-ttu-id="595ae-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="595ae-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="595ae-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="595ae-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595ae-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="595ae-107">DESCRIPTION</span></span>
<span data-ttu-id="595ae-108">**Remove-AzVmssExtension** cmdlet 'ı sanal makine ölçek kümesinden (VMSS) uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="595ae-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="595ae-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="595ae-109">EXAMPLES</span></span>

### <span data-ttu-id="595ae-110">Örnek 1: VMSS 'den uzantıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="595ae-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="595ae-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="595ae-111">PARAMETERS</span></span>

### <span data-ttu-id="595ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595ae-112">-DefaultProfile</span></span>
<span data-ttu-id="595ae-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="595ae-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="595ae-114">-ID</span><span class="sxs-lookup"><span data-stu-id="595ae-114">-Id</span></span>
<span data-ttu-id="595ae-115">Bu cmdlet 'in VMSUBNET 'den kaldırdığı uzantının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="595ae-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595ae-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="595ae-116">-Name</span></span>
<span data-ttu-id="595ae-117">Bu cmdlet 'in kaldırıldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="595ae-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595ae-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="595ae-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="595ae-119">Uzantısının kaldırılacağı VMSS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="595ae-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="595ae-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="595ae-120">-Confirm</span></span>
<span data-ttu-id="595ae-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="595ae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="595ae-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595ae-122">-WhatIf</span></span>
<span data-ttu-id="595ae-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="595ae-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="595ae-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="595ae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="595ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595ae-125">CommonParameters</span></span>
<span data-ttu-id="595ae-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="595ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595ae-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="595ae-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595ae-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="595ae-128">INPUTS</span></span>

### <span data-ttu-id="595ae-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="595ae-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="595ae-130">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="595ae-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="595ae-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="595ae-131">OUTPUTS</span></span>

### <span data-ttu-id="595ae-132">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="595ae-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="595ae-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="595ae-133">NOTES</span></span>

## <span data-ttu-id="595ae-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="595ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="595ae-135">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="595ae-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
