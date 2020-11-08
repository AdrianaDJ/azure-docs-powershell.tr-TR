---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939748"
---
# <span data-ttu-id="e8bdd-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e8bdd-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="e8bdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bdd-103">Sanal makineden özel bir komut dosyası uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8bdd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8bdd-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8bdd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bdd-106">**Remove-AzureRmVMCustomScriptExtension** cmdlet 'i sanal makineden özel betik sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="e8bdd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8bdd-107">EXAMPLES</span></span>

## <span data-ttu-id="e8bdd-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8bdd-108">PARAMETERS</span></span>

### <span data-ttu-id="e8bdd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bdd-109">-DefaultProfile</span></span>
<span data-ttu-id="e8bdd-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8bdd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e8bdd-111">-Force</span></span>
<span data-ttu-id="e8bdd-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e8bdd-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8bdd-113">-Name</span></span>
<span data-ttu-id="e8bdd-114">Bu cmdlet 'in kaldırıldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e8bdd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8bdd-115">-ResourceGroupName</span></span>
<span data-ttu-id="e8bdd-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e8bdd-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="e8bdd-117">-VMName</span></span>
<span data-ttu-id="e8bdd-118">Bu cmdlet 'in özel komut dosyası uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="e8bdd-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8bdd-119">-Confirm</span></span>
<span data-ttu-id="e8bdd-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8bdd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8bdd-121">-WhatIf</span></span>
<span data-ttu-id="e8bdd-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e8bdd-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8bdd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bdd-124">CommonParameters</span></span>
<span data-ttu-id="e8bdd-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bdd-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8bdd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bdd-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8bdd-127">INPUTS</span></span>

### <span data-ttu-id="e8bdd-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e8bdd-128">None</span></span>
<span data-ttu-id="e8bdd-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e8bdd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8bdd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8bdd-130">OUTPUTS</span></span>

### <span data-ttu-id="e8bdd-131">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e8bdd-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e8bdd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8bdd-132">NOTES</span></span>

## <span data-ttu-id="e8bdd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8bdd-133">RELATED LINKS</span></span>

[<span data-ttu-id="e8bdd-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e8bdd-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="e8bdd-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e8bdd-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)