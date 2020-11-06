---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 2d1edd8e511042f677928f171d7e31859cc5390f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586976"
---
# <span data-ttu-id="84b30-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="84b30-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="84b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84b30-102">SYNOPSIS</span></span>
<span data-ttu-id="84b30-103">Sanal makineden özel bir komut dosyası uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84b30-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84b30-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84b30-105">DESCRIPTION</span></span>
<span data-ttu-id="84b30-106">**Remove-AzureRmVMCustomScriptExtension** cmdlet 'i sanal makineden özel betik sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84b30-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="84b30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84b30-107">EXAMPLES</span></span>

## <span data-ttu-id="84b30-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84b30-108">PARAMETERS</span></span>

### <span data-ttu-id="84b30-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b30-109">-DefaultProfile</span></span>
<span data-ttu-id="84b30-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84b30-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b30-111">-Force</span><span class="sxs-lookup"><span data-stu-id="84b30-111">-Force</span></span>
<span data-ttu-id="84b30-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="84b30-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="84b30-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="84b30-113">-Name</span></span>
<span data-ttu-id="84b30-114">Bu cmdlet 'in kaldırıldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84b30-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="84b30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b30-115">-ResourceGroupName</span></span>
<span data-ttu-id="84b30-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84b30-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="84b30-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="84b30-117">-VMName</span></span>
<span data-ttu-id="84b30-118">Bu cmdlet 'in özel komut dosyası uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84b30-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="84b30-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="84b30-119">-Confirm</span></span>
<span data-ttu-id="84b30-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84b30-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b30-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b30-121">-WhatIf</span></span>
<span data-ttu-id="84b30-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84b30-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="84b30-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84b30-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b30-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b30-124">CommonParameters</span></span>
<span data-ttu-id="84b30-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84b30-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b30-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b30-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b30-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84b30-127">INPUTS</span></span>

## <span data-ttu-id="84b30-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84b30-128">OUTPUTS</span></span>

## <span data-ttu-id="84b30-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84b30-129">NOTES</span></span>

## <span data-ttu-id="84b30-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84b30-130">RELATED LINKS</span></span>

[<span data-ttu-id="84b30-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="84b30-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="84b30-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="84b30-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
