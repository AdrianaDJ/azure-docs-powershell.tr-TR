---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 9256828a338678cb1da12e14cb6e450ee4030ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752788"
---
# <span data-ttu-id="4b72a-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b72a-101">Remove-AzVM</span></span>

## <span data-ttu-id="4b72a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b72a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b72a-103">Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b72a-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="4b72a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b72a-104">SYNTAX</span></span>

### <span data-ttu-id="4b72a-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b72a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b72a-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="4b72a-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b72a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b72a-107">DESCRIPTION</span></span>
<span data-ttu-id="4b72a-108">**Remove-AzVM** cmdlet 'i Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b72a-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="4b72a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b72a-109">EXAMPLES</span></span>

### <span data-ttu-id="4b72a-110">Örnek 1: sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="4b72a-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="4b72a-111">Bu komut, kaynak grubundaki VirtualMachine07 adındaki sanal makineyi kaldırır ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4b72a-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="4b72a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b72a-112">PARAMETERS</span></span>

### <span data-ttu-id="4b72a-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="4b72a-113">-AsJob</span></span>
<span data-ttu-id="4b72a-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="4b72a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4b72a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b72a-115">-DefaultProfile</span></span>
<span data-ttu-id="4b72a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b72a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b72a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4b72a-117">-Force</span></span>
<span data-ttu-id="4b72a-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4b72a-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b72a-119">-ID</span><span class="sxs-lookup"><span data-stu-id="4b72a-119">-Id</span></span>
<span data-ttu-id="4b72a-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4b72a-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b72a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b72a-121">-Name</span></span>
<span data-ttu-id="4b72a-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4b72a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b72a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4b72a-123">-NoWait</span></span>
<span data-ttu-id="4b72a-124">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="4b72a-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4b72a-125">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="4b72a-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4b72a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b72a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b72a-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b72a-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b72a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b72a-128">-Confirm</span></span>
<span data-ttu-id="4b72a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b72a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b72a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b72a-130">-WhatIf</span></span>
<span data-ttu-id="4b72a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b72a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b72a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b72a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b72a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b72a-133">CommonParameters</span></span>
<span data-ttu-id="4b72a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b72a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b72a-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b72a-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b72a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b72a-136">INPUTS</span></span>

### <span data-ttu-id="4b72a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4b72a-137">System.String</span></span>

## <span data-ttu-id="4b72a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b72a-138">OUTPUTS</span></span>

### <span data-ttu-id="4b72a-139">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="4b72a-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="4b72a-140">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4b72a-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4b72a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b72a-141">NOTES</span></span>

## <span data-ttu-id="4b72a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b72a-142">RELATED LINKS</span></span>

[<span data-ttu-id="4b72a-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b72a-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4b72a-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b72a-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="4b72a-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b72a-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="4b72a-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b72a-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="4b72a-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b72a-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="4b72a-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b72a-148">Update-AzVM</span></span>](./Update-AzVM.md)


