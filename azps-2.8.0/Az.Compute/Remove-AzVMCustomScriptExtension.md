---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752776"
---
# <span data-ttu-id="cfaf5-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfaf5-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="cfaf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="cfaf5-103">Sanal makineden özel bir komut dosyası uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="cfaf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfaf5-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfaf5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfaf5-105">DESCRIPTION</span></span>
<span data-ttu-id="cfaf5-106">**Remove-AzVMCustomScriptExtension** cmdlet 'i, bir sanal makineden özel betik sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="cfaf5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfaf5-107">EXAMPLES</span></span>

## <span data-ttu-id="cfaf5-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfaf5-108">PARAMETERS</span></span>

### <span data-ttu-id="cfaf5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfaf5-109">-DefaultProfile</span></span>
<span data-ttu-id="cfaf5-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfaf5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="cfaf5-111">-Force</span></span>
<span data-ttu-id="cfaf5-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cfaf5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="cfaf5-113">-Name</span></span>
<span data-ttu-id="cfaf5-114">Bu cmdlet 'in kaldırıldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf5-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cfaf5-115">-NoWait</span></span>
<span data-ttu-id="cfaf5-116">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cfaf5-117">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cfaf5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfaf5-118">-ResourceGroupName</span></span>
<span data-ttu-id="cfaf5-119">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cfaf5-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="cfaf5-120">-VMName</span></span>
<span data-ttu-id="cfaf5-121">Bu cmdlet 'in özel komut dosyası uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="cfaf5-122">-Confirm</span></span>
<span data-ttu-id="cfaf5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfaf5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfaf5-124">-WhatIf</span></span>
<span data-ttu-id="cfaf5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfaf5-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfaf5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfaf5-127">CommonParameters</span></span>
<span data-ttu-id="cfaf5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfaf5-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cfaf5-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfaf5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfaf5-130">INPUTS</span></span>

### <span data-ttu-id="cfaf5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cfaf5-131">System.String</span></span>

## <span data-ttu-id="cfaf5-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfaf5-132">OUTPUTS</span></span>

### <span data-ttu-id="cfaf5-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cfaf5-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cfaf5-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfaf5-134">NOTES</span></span>

## <span data-ttu-id="cfaf5-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfaf5-135">RELATED LINKS</span></span>

[<span data-ttu-id="cfaf5-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfaf5-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="cfaf5-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfaf5-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
