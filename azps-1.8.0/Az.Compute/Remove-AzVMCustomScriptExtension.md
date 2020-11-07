---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 83041e17a930ee63c17f68d6ce8ce2797a25318c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761282"
---
# <span data-ttu-id="47b0c-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="47b0c-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="47b0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="47b0c-103">Sanal makineden özel bir komut dosyası uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47b0c-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="47b0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47b0c-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b0c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="47b0c-106">**Remove-AzVMCustomScriptExtension** cmdlet 'i, bir sanal makineden özel betik sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47b0c-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="47b0c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47b0c-107">EXAMPLES</span></span>

## <span data-ttu-id="47b0c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47b0c-108">PARAMETERS</span></span>

### <span data-ttu-id="47b0c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b0c-109">-DefaultProfile</span></span>
<span data-ttu-id="47b0c-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47b0c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47b0c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="47b0c-111">-Force</span></span>
<span data-ttu-id="47b0c-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="47b0c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47b0c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="47b0c-113">-Name</span></span>
<span data-ttu-id="47b0c-114">Bu cmdlet 'in kaldırıldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47b0c-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="47b0c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b0c-115">-ResourceGroupName</span></span>
<span data-ttu-id="47b0c-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47b0c-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="47b0c-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="47b0c-117">-VMName</span></span>
<span data-ttu-id="47b0c-118">Bu cmdlet 'in özel komut dosyası uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47b0c-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="47b0c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="47b0c-119">-Confirm</span></span>
<span data-ttu-id="47b0c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47b0c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b0c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b0c-121">-WhatIf</span></span>
<span data-ttu-id="47b0c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47b0c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b0c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47b0c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b0c-124">CommonParameters</span></span>
<span data-ttu-id="47b0c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47b0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b0c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b0c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b0c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47b0c-127">INPUTS</span></span>

### <span data-ttu-id="47b0c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="47b0c-128">System.String</span></span>

## <span data-ttu-id="47b0c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47b0c-129">OUTPUTS</span></span>

### <span data-ttu-id="47b0c-130">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="47b0c-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="47b0c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47b0c-131">NOTES</span></span>

## <span data-ttu-id="47b0c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47b0c-132">RELATED LINKS</span></span>

[<span data-ttu-id="47b0c-133">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="47b0c-133">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="47b0c-134">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="47b0c-134">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)