---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: c1280b6e59b4dc1c4ddd70b924863eacce0c6e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936892"
---
# <span data-ttu-id="b535a-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b535a-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="b535a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b535a-102">SYNOPSIS</span></span>
<span data-ttu-id="b535a-103">Bir tanılama uzantısını VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b535a-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="b535a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b535a-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b535a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b535a-105">DESCRIPTION</span></span>
<span data-ttu-id="b535a-106">**Remove-Azvmssdiagnosticsextenma** cmdlet 'ı, sanal makine ölçek kümesinden (VMSS) bir tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b535a-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b535a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b535a-107">EXAMPLES</span></span>

### <span data-ttu-id="b535a-108">Örnek 1: VMSS 'den tanılama uzantısı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b535a-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="b535a-109">Bu komut, VMSS 'den tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b535a-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="b535a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b535a-110">PARAMETERS</span></span>

### <span data-ttu-id="b535a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b535a-111">-DefaultProfile</span></span>
<span data-ttu-id="b535a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b535a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b535a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b535a-113">-Name</span></span>
<span data-ttu-id="b535a-114">Bu cmdlet 'in kaldırıldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b535a-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b535a-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b535a-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b535a-116">Uzantının kaldırılacağı VMSS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b535a-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="b535a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b535a-117">-Confirm</span></span>
<span data-ttu-id="b535a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b535a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b535a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b535a-119">-WhatIf</span></span>
<span data-ttu-id="b535a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b535a-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b535a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b535a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b535a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b535a-122">CommonParameters</span></span>
<span data-ttu-id="b535a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b535a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b535a-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b535a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b535a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b535a-125">INPUTS</span></span>

### <span data-ttu-id="b535a-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b535a-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="b535a-127">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b535a-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="b535a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b535a-128">OUTPUTS</span></span>

###  
<span data-ttu-id="b535a-129">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b535a-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b535a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b535a-130">NOTES</span></span>

## <span data-ttu-id="b535a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b535a-131">RELATED LINKS</span></span>

[<span data-ttu-id="b535a-132">Add-azvmssdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="b535a-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="b535a-133">Remove-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="b535a-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="b535a-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b535a-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


