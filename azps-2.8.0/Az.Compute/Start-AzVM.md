---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 08fa41232a6f473b371c0e44e22b21712f61f1b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752657"
---
# <span data-ttu-id="d0052-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0052-101">Start-AzVM</span></span>

## <span data-ttu-id="d0052-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0052-102">SYNOPSIS</span></span>
<span data-ttu-id="d0052-103">Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0052-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="d0052-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0052-104">SYNTAX</span></span>

### <span data-ttu-id="d0052-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d0052-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0052-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="d0052-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0052-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0052-107">DESCRIPTION</span></span>
<span data-ttu-id="d0052-108">**Start-AzVM** cmdlet 'ı bir Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0052-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="d0052-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0052-109">EXAMPLES</span></span>

### <span data-ttu-id="d0052-110">Örnek 1: sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="d0052-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d0052-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0052-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="d0052-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0052-112">PARAMETERS</span></span>

### <span data-ttu-id="d0052-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d0052-113">-AsJob</span></span>
<span data-ttu-id="d0052-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="d0052-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d0052-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0052-115">-DefaultProfile</span></span>
<span data-ttu-id="d0052-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0052-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0052-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d0052-117">-Id</span></span>
<span data-ttu-id="d0052-118">Sanal makinenin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d0052-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="d0052-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0052-119">-Name</span></span>
<span data-ttu-id="d0052-120">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="d0052-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0052-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0052-121">-NoWait</span></span>
<span data-ttu-id="d0052-122">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="d0052-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d0052-123">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0052-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d0052-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0052-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0052-125">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0052-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d0052-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0052-126">-Confirm</span></span>
<span data-ttu-id="d0052-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0052-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0052-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0052-128">-WhatIf</span></span>
<span data-ttu-id="d0052-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0052-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0052-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0052-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0052-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0052-131">CommonParameters</span></span>
<span data-ttu-id="d0052-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0052-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0052-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d0052-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0052-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0052-134">INPUTS</span></span>

### <span data-ttu-id="d0052-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d0052-135">System.String</span></span>

## <span data-ttu-id="d0052-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0052-136">OUTPUTS</span></span>

### <span data-ttu-id="d0052-137">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d0052-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="d0052-138">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d0052-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d0052-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0052-139">NOTES</span></span>

## <span data-ttu-id="d0052-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0052-140">RELATED LINKS</span></span>

[<span data-ttu-id="d0052-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0052-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d0052-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0052-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d0052-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0052-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d0052-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0052-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d0052-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0052-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d0052-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0052-146">Update-AzVM</span></span>](./Update-AzVM.md)


