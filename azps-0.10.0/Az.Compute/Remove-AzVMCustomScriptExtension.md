---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936916"
---
# <span data-ttu-id="0b9f5-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0b9f5-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="0b9f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9f5-103">Sanal makineden özel bir komut dosyası uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="0b9f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b9f5-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b9f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b9f5-105">DESCRIPTION</span></span>
<span data-ttu-id="0b9f5-106">**Remove-AzVMCustomScriptExtension** cmdlet 'i, bir sanal makineden özel betik sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="0b9f5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b9f5-107">EXAMPLES</span></span>

## <span data-ttu-id="0b9f5-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b9f5-108">PARAMETERS</span></span>

### <span data-ttu-id="0b9f5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9f5-109">-DefaultProfile</span></span>
<span data-ttu-id="0b9f5-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b9f5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0b9f5-111">-Force</span></span>
<span data-ttu-id="0b9f5-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9f5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b9f5-113">-Name</span></span>
<span data-ttu-id="0b9f5-114">Bu cmdlet 'in kaldırıldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b9f5-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0b9f5-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="0b9f5-117">-VMName</span></span>
<span data-ttu-id="0b9f5-118">Bu cmdlet 'in özel komut dosyası uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9f5-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b9f5-119">-Confirm</span></span>
<span data-ttu-id="0b9f5-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b9f5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b9f5-121">-WhatIf</span></span>
<span data-ttu-id="0b9f5-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0b9f5-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b9f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9f5-124">CommonParameters</span></span>
<span data-ttu-id="0b9f5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9f5-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b9f5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9f5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b9f5-127">INPUTS</span></span>

### <span data-ttu-id="0b9f5-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b9f5-128">None</span></span>
<span data-ttu-id="0b9f5-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b9f5-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b9f5-130">OUTPUTS</span></span>

### <span data-ttu-id="0b9f5-131">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b9f5-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0b9f5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b9f5-132">NOTES</span></span>

## <span data-ttu-id="0b9f5-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b9f5-133">RELATED LINKS</span></span>

[<span data-ttu-id="0b9f5-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0b9f5-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="0b9f5-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0b9f5-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
