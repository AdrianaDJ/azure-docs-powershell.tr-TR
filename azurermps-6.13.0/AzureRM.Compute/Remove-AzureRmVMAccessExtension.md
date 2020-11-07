---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0360bcdb766de681ab6f54682007076e18266051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762119"
---
# <span data-ttu-id="e97c7-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="e97c7-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="e97c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e97c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e97c7-103">Sanal makineden VMAccess uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e97c7-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e97c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e97c7-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e97c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e97c7-105">DESCRIPTION</span></span>
<span data-ttu-id="e97c7-106">**Remove-Azurermvmaccessextenma** cmdlet 'i sanal makine erişimi (VMAccess) sanal makine uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e97c7-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="e97c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e97c7-107">EXAMPLES</span></span>

## <span data-ttu-id="e97c7-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e97c7-108">PARAMETERS</span></span>

### <span data-ttu-id="e97c7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97c7-109">-DefaultProfile</span></span>
<span data-ttu-id="e97c7-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e97c7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e97c7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e97c7-111">-Force</span></span>
<span data-ttu-id="e97c7-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e97c7-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e97c7-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e97c7-113">-Name</span></span>
<span data-ttu-id="e97c7-114">Bu cmdlet 'in kaldırdığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e97c7-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e97c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e97c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e97c7-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e97c7-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e97c7-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="e97c7-117">-VMName</span></span>
<span data-ttu-id="e97c7-118">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e97c7-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e97c7-119">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e97c7-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e97c7-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="e97c7-120">-Confirm</span></span>
<span data-ttu-id="e97c7-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e97c7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e97c7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e97c7-122">-WhatIf</span></span>
<span data-ttu-id="e97c7-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e97c7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e97c7-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e97c7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e97c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97c7-125">CommonParameters</span></span>
<span data-ttu-id="e97c7-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e97c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97c7-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e97c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97c7-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e97c7-128">INPUTS</span></span>

### <span data-ttu-id="e97c7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e97c7-129">System.String</span></span>

## <span data-ttu-id="e97c7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e97c7-130">OUTPUTS</span></span>

### <span data-ttu-id="e97c7-131">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e97c7-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e97c7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e97c7-132">NOTES</span></span>

## <span data-ttu-id="e97c7-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e97c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="e97c7-134">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="e97c7-134">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="e97c7-135">Set-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="e97c7-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="e97c7-136">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="e97c7-136">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)