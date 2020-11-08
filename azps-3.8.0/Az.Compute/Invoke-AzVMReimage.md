---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096963"
---
# <span data-ttu-id="2f6e3-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2f6e3-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="2f6e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6e3-103">Azure sanal makinesini yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="2f6e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f6e3-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f6e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f6e3-105">DESCRIPTION</span></span>
<span data-ttu-id="2f6e3-106">**Invoke-Azvmreımage** cmdlet 'ı bir Azure sanal makinesini yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="2f6e3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f6e3-107">EXAMPLES</span></span>

### <span data-ttu-id="2f6e3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f6e3-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2f6e3-109">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2f6e3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f6e3-110">PARAMETERS</span></span>

### <span data-ttu-id="2f6e3-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2f6e3-111">-AsJob</span></span>
<span data-ttu-id="2f6e3-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2f6e3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f6e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6e3-113">-DefaultProfile</span></span>
<span data-ttu-id="2f6e3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f6e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f6e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="2f6e3-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2f6e3-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="2f6e3-117">-TempDisk</span></span>
<span data-ttu-id="2f6e3-118">Geçici diske yeniden görüntü uygulanıp gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="2f6e3-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="2f6e3-119">-VMName</span></span>
<span data-ttu-id="2f6e3-120">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6e3-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f6e3-121">-Confirm</span></span>
<span data-ttu-id="2f6e3-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f6e3-123">-WhatIf</span></span>
<span data-ttu-id="2f6e3-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f6e3-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6e3-126">CommonParameters</span></span>
<span data-ttu-id="2f6e3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6e3-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2f6e3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6e3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f6e3-129">INPUTS</span></span>

### <span data-ttu-id="2f6e3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f6e3-130">System.String</span></span>

## <span data-ttu-id="2f6e3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f6e3-131">OUTPUTS</span></span>

### <span data-ttu-id="2f6e3-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="2f6e3-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2f6e3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f6e3-133">NOTES</span></span>

## <span data-ttu-id="2f6e3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f6e3-134">RELATED LINKS</span></span>
