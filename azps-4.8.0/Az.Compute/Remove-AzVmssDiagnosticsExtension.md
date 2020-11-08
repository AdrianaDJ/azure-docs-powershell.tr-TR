---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268578"
---
# <span data-ttu-id="d3eb9-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d3eb9-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="d3eb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="d3eb9-103">Bir tanılama uzantısını VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="d3eb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3eb9-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3eb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="d3eb9-106">**Remove-Azvmssdiagnosticsextenma** cmdlet 'ı, sanal makine ölçek kümesinden (VMSS) bir tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d3eb9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="d3eb9-108">Örnek 1: VMSS 'den tanılama uzantısı kaldırma</span><span class="sxs-lookup"><span data-stu-id="d3eb9-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="d3eb9-109">Bu komut, VMSS 'den tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="d3eb9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3eb9-110">PARAMETERS</span></span>

### <span data-ttu-id="d3eb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3eb9-111">-DefaultProfile</span></span>
<span data-ttu-id="d3eb9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3eb9-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3eb9-113">-Name</span></span>
<span data-ttu-id="d3eb9-114">Bu cmdlet 'in kaldırıldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eb9-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d3eb9-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d3eb9-116">Uzantının kaldırılacağı VMSS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="d3eb9-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3eb9-117">-Confirm</span></span>
<span data-ttu-id="d3eb9-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3eb9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3eb9-119">-WhatIf</span></span>
<span data-ttu-id="d3eb9-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3eb9-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3eb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3eb9-122">CommonParameters</span></span>
<span data-ttu-id="d3eb9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3eb9-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3eb9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3eb9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3eb9-125">INPUTS</span></span>

### <span data-ttu-id="d3eb9-126">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d3eb9-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d3eb9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3eb9-127">System.String</span></span>

## <span data-ttu-id="d3eb9-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3eb9-128">OUTPUTS</span></span>

### <span data-ttu-id="d3eb9-129">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d3eb9-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d3eb9-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3eb9-130">NOTES</span></span>

## <span data-ttu-id="d3eb9-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3eb9-131">RELATED LINKS</span></span>

[<span data-ttu-id="d3eb9-132">Add-azvmssdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="d3eb9-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="d3eb9-133">Remove-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="d3eb9-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="d3eb9-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d3eb9-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


