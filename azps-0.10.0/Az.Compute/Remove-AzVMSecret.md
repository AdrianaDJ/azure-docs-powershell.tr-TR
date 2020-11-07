---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: da904e6dfbf9d85319636b3bc6ff5ced5f0b2973
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936903"
---
# <span data-ttu-id="75541-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="75541-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="75541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75541-102">SYNOPSIS</span></span>
<span data-ttu-id="75541-103">Sanal makine nesnesinden gizli (a) gizli kod çıkarır</span><span class="sxs-lookup"><span data-stu-id="75541-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="75541-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75541-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75541-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75541-105">DESCRIPTION</span></span>
<span data-ttu-id="75541-106">Remove-AzVMSecret cmdlet 'i sanal makine nesnesinden gizli (bir) parolayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="75541-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="75541-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75541-107">EXAMPLES</span></span>

### <span data-ttu-id="75541-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="75541-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="75541-109">"RG1" kaynak grubundaki "VM1" sanal makinesindeki tüm gizlilikleri kaldırır ve VM 'yi güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="75541-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="75541-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75541-110">PARAMETERS</span></span>

### <span data-ttu-id="75541-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75541-111">-DefaultProfile</span></span>
<span data-ttu-id="75541-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75541-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75541-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="75541-113">-SourceVaultId</span></span>
<span data-ttu-id="75541-114">Bu cmdlet 'in kaldırdığı kaynak Kasası kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75541-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="75541-115">-VM</span><span class="sxs-lookup"><span data-stu-id="75541-115">-VM</span></span>
<span data-ttu-id="75541-116">Bu cmdlet 'in kaldırıldığı (a) gizli (a) sanal makinesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75541-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="75541-117">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="75541-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="75541-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="75541-118">-Confirm</span></span>
<span data-ttu-id="75541-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75541-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75541-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75541-120">-WhatIf</span></span>
<span data-ttu-id="75541-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75541-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75541-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75541-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75541-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75541-123">CommonParameters</span></span>
<span data-ttu-id="75541-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75541-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75541-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75541-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75541-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75541-126">INPUTS</span></span>

### <span data-ttu-id="75541-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="75541-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="75541-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75541-128">OUTPUTS</span></span>

### <span data-ttu-id="75541-129">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="75541-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="75541-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75541-130">NOTES</span></span>

## <span data-ttu-id="75541-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75541-131">RELATED LINKS</span></span>

