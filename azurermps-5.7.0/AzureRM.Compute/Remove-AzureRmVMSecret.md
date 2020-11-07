---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 84f8abc6c298d7c82bef2494086deef3e4130842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762751"
---
# <span data-ttu-id="e13ce-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="e13ce-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="e13ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e13ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e13ce-103">Sanal makine nesnesinden gizli (a) gizli kod çıkarır</span><span class="sxs-lookup"><span data-stu-id="e13ce-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e13ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e13ce-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e13ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e13ce-105">DESCRIPTION</span></span>
<span data-ttu-id="e13ce-106">Remove-AzureRmVMSecret cmdlet 'i sanal makine nesnesinden gizli (bir) parolayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e13ce-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="e13ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e13ce-107">EXAMPLES</span></span>

### <span data-ttu-id="e13ce-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e13ce-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="e13ce-109">"RG1" kaynak grubundaki "VM1" sanal makinesindeki tüm gizlilikleri kaldırır ve VM 'yi güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="e13ce-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="e13ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e13ce-110">PARAMETERS</span></span>

### <span data-ttu-id="e13ce-111">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e13ce-111">-SourceVaultId</span></span>
<span data-ttu-id="e13ce-112">Bu cmdlet 'in kaldırdığı kaynak Kasası kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e13ce-112">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e13ce-113">-VM</span><span class="sxs-lookup"><span data-stu-id="e13ce-113">-VM</span></span>
<span data-ttu-id="e13ce-114">Bu cmdlet 'in kaldırıldığı (a) gizli (a) sanal makinesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e13ce-114">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="e13ce-115">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e13ce-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e13ce-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="e13ce-116">-Confirm</span></span>
<span data-ttu-id="e13ce-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e13ce-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e13ce-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e13ce-118">-WhatIf</span></span>
<span data-ttu-id="e13ce-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e13ce-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e13ce-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e13ce-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e13ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13ce-121">CommonParameters</span></span>
<span data-ttu-id="e13ce-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e13ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13ce-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13ce-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13ce-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e13ce-124">INPUTS</span></span>

### <span data-ttu-id="e13ce-125">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e13ce-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e13ce-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e13ce-126">OUTPUTS</span></span>

### <span data-ttu-id="e13ce-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e13ce-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e13ce-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e13ce-128">NOTES</span></span>

## <span data-ttu-id="e13ce-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e13ce-129">RELATED LINKS</span></span>

