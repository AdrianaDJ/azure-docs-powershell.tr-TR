---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 9f9b8f28fd3b2597dede1b9fe50780b2c5e43abb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761275"
---
# <span data-ttu-id="5cfc5-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="5cfc5-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="5cfc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="5cfc5-103">Sanal makine nesnesinden gizli (a) gizli kod çıkarır</span><span class="sxs-lookup"><span data-stu-id="5cfc5-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="5cfc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cfc5-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cfc5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cfc5-105">DESCRIPTION</span></span>
<span data-ttu-id="5cfc5-106">Remove-AzVMSecret cmdlet 'i sanal makine nesnesinden gizli (bir) parolayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="5cfc5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cfc5-107">EXAMPLES</span></span>

### <span data-ttu-id="5cfc5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5cfc5-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="5cfc5-109">"RG1" kaynak grubundaki "VM1" sanal makinesindeki tüm gizlilikleri kaldırır ve VM 'yi güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="5cfc5-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="5cfc5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cfc5-110">PARAMETERS</span></span>

### <span data-ttu-id="5cfc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cfc5-111">-DefaultProfile</span></span>
<span data-ttu-id="5cfc5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cfc5-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5cfc5-113">-SourceVaultId</span></span>
<span data-ttu-id="5cfc5-114">Bu cmdlet 'in kaldırdığı kaynak Kasası kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cfc5-115">-VM</span><span class="sxs-lookup"><span data-stu-id="5cfc5-115">-VM</span></span>
<span data-ttu-id="5cfc5-116">Bu cmdlet 'in kaldırıldığı (a) gizli (a) sanal makinesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="5cfc5-117">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfc5-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cfc5-118">-Confirm</span></span>
<span data-ttu-id="5cfc5-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cfc5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cfc5-120">-WhatIf</span></span>
<span data-ttu-id="5cfc5-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cfc5-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cfc5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cfc5-123">CommonParameters</span></span>
<span data-ttu-id="5cfc5-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cfc5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cfc5-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cfc5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cfc5-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cfc5-126">INPUTS</span></span>

### <span data-ttu-id="5cfc5-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5cfc5-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5cfc5-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cfc5-128">OUTPUTS</span></span>

### <span data-ttu-id="5cfc5-129">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5cfc5-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5cfc5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cfc5-130">NOTES</span></span>

## <span data-ttu-id="5cfc5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cfc5-131">RELATED LINKS</span></span>
