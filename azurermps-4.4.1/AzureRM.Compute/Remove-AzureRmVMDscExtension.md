---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: d192d00be7de4561f8186671c17cca7328b0269f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586966"
---
# <span data-ttu-id="e0aec-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e0aec-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="e0aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0aec-102">SYNOPSIS</span></span>
<span data-ttu-id="e0aec-103">Bir kaynak grubundaki sanal makineden DSC genişletme işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0aec-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0aec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0aec-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0aec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0aec-105">DESCRIPTION</span></span>
<span data-ttu-id="e0aec-106">**Remove-AzureRmVMDscExtension** cmdlet 'i, bir kaynak grubundaki sanal makineden Istenen durum yapılandırma (DSC) uzantı işleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0aec-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="e0aec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0aec-107">EXAMPLES</span></span>

### <span data-ttu-id="e0aec-108">Örnek 1: DSC uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e0aec-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResouceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="e0aec-109">Bu komut, VM07 adındaki sanal makinede DSC adlı uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0aec-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="e0aec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0aec-110">PARAMETERS</span></span>

### <span data-ttu-id="e0aec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0aec-111">-DefaultProfile</span></span>
<span data-ttu-id="e0aec-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0aec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0aec-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0aec-113">-Name</span></span>
<span data-ttu-id="e0aec-114">Bu cmdlet 'in kaldırıldığı DSC uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0aec-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="e0aec-115">Set-AzureRmVMDscExtension cmdlet, **Remove-AzureRmVMDscExtension** tarafından kullanılan varsayılan değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e0aec-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0aec-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0aec-116">-ResourceGroupName</span></span>
<span data-ttu-id="e0aec-117">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0aec-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e0aec-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="e0aec-118">-VMName</span></span>
<span data-ttu-id="e0aec-119">Bu cmdlet 'in DSC uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0aec-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0aec-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0aec-120">-Confirm</span></span>
<span data-ttu-id="e0aec-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0aec-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0aec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0aec-122">-WhatIf</span></span>
<span data-ttu-id="e0aec-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0aec-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e0aec-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0aec-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0aec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0aec-125">CommonParameters</span></span>
<span data-ttu-id="e0aec-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0aec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0aec-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0aec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0aec-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0aec-128">INPUTS</span></span>

## <span data-ttu-id="e0aec-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0aec-129">OUTPUTS</span></span>

## <span data-ttu-id="e0aec-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0aec-130">NOTES</span></span>

## <span data-ttu-id="e0aec-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0aec-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0aec-132">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e0aec-132">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="e0aec-133">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e0aec-133">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


