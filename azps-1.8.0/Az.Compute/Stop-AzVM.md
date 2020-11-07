---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 393f2a75217b95b6c1c5366326735ac0f78ac294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917200"
---
# <span data-ttu-id="26e87-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="26e87-101">Stop-AzVM</span></span>

## <span data-ttu-id="26e87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e87-102">SYNOPSIS</span></span>
<span data-ttu-id="26e87-103">Bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="26e87-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="26e87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26e87-104">SYNTAX</span></span>

### <span data-ttu-id="26e87-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26e87-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e87-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="26e87-106">IdParameterSetName</span></span>
```
Stop-AzVM [[-Name] <String>] [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e87-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="26e87-107">DESCRIPTION</span></span>
<span data-ttu-id="26e87-108">**Stop-AzVM** cmdlet 'ı bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="26e87-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="26e87-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26e87-109">EXAMPLES</span></span>

### <span data-ttu-id="26e87-110">Örnek 1: sanal makineyi durdurma</span><span class="sxs-lookup"><span data-stu-id="26e87-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="26e87-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="26e87-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="26e87-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26e87-112">PARAMETERS</span></span>

### <span data-ttu-id="26e87-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="26e87-113">-AsJob</span></span>
<span data-ttu-id="26e87-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="26e87-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="26e87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e87-115">-DefaultProfile</span></span>
<span data-ttu-id="26e87-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26e87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26e87-117">-Force</span><span class="sxs-lookup"><span data-stu-id="26e87-117">-Force</span></span>
<span data-ttu-id="26e87-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="26e87-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26e87-119">-ID</span><span class="sxs-lookup"><span data-stu-id="26e87-119">-Id</span></span>
<span data-ttu-id="26e87-120">Sanal makinenin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="26e87-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="26e87-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="26e87-121">-Name</span></span>
<span data-ttu-id="26e87-122">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="26e87-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e87-123">-ResourceGroupName</span></span>
<span data-ttu-id="26e87-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e87-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="26e87-125">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="26e87-125">-StayProvisioned</span></span>
<span data-ttu-id="26e87-126">Cmdlet, VMSS içindeki tüm sanal makineleri durdurur ancak bunları serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="26e87-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="26e87-127">Hesap, durdurulan sanal makineler için ücretlendirilecek.</span><span class="sxs-lookup"><span data-stu-id="26e87-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="26e87-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="26e87-128">-Confirm</span></span>
<span data-ttu-id="26e87-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26e87-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e87-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e87-130">-WhatIf</span></span>
<span data-ttu-id="26e87-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26e87-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26e87-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26e87-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e87-133">CommonParameters</span></span>
<span data-ttu-id="26e87-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26e87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e87-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e87-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e87-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26e87-136">INPUTS</span></span>

### <span data-ttu-id="26e87-137">System. String</span><span class="sxs-lookup"><span data-stu-id="26e87-137">System.String</span></span>

## <span data-ttu-id="26e87-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26e87-138">OUTPUTS</span></span>

### <span data-ttu-id="26e87-139">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="26e87-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="26e87-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26e87-140">NOTES</span></span>

## <span data-ttu-id="26e87-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26e87-141">RELATED LINKS</span></span>

[<span data-ttu-id="26e87-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="26e87-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="26e87-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="26e87-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="26e87-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="26e87-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="26e87-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="26e87-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="26e87-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="26e87-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="26e87-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="26e87-147">Update-AzVM</span></span>](./Update-AzVM.md)


