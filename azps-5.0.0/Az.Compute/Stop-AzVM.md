---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276772"
---
# <span data-ttu-id="4ed5f-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ed5f-101">Stop-AzVM</span></span>

## <span data-ttu-id="4ed5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed5f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed5f-103">Bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="4ed5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ed5f-104">SYNTAX</span></span>

### <span data-ttu-id="4ed5f-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ed5f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed5f-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="4ed5f-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed5f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ed5f-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed5f-108">**Stop-AzVM** cmdlet 'ı bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="4ed5f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ed5f-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed5f-110">Örnek 1: sanal makineyi durdurma</span><span class="sxs-lookup"><span data-stu-id="4ed5f-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="4ed5f-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="4ed5f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ed5f-112">PARAMETERS</span></span>

### <span data-ttu-id="4ed5f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="4ed5f-113">-AsJob</span></span>
<span data-ttu-id="4ed5f-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4ed5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed5f-115">-DefaultProfile</span></span>
<span data-ttu-id="4ed5f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed5f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4ed5f-117">-Force</span></span>
<span data-ttu-id="4ed5f-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ed5f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="4ed5f-119">-Id</span></span>
<span data-ttu-id="4ed5f-120">Sanal makinenin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="4ed5f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ed5f-121">-Name</span></span>
<span data-ttu-id="4ed5f-122">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="4ed5f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4ed5f-123">-NoWait</span></span>
<span data-ttu-id="4ed5f-124">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4ed5f-125">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4ed5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ed5f-127">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4ed5f-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="4ed5f-128">-SkipShutdown</span></span>
<span data-ttu-id="4ed5f-129">Sağlanan VM 'yi korurken düzgün olmayan bir VM kapatması istemek için.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="4ed5f-130">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="4ed5f-130">-StayProvisioned</span></span>
<span data-ttu-id="4ed5f-131">Cmdlet, VMSS içindeki tüm sanal makineleri durdurur ancak bunları serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="4ed5f-132">Hesap, durdurulan sanal makineler için ücretlendirilecek.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="4ed5f-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ed5f-133">-Confirm</span></span>
<span data-ttu-id="4ed5f-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed5f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed5f-135">-WhatIf</span></span>
<span data-ttu-id="4ed5f-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ed5f-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed5f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed5f-138">CommonParameters</span></span>
<span data-ttu-id="4ed5f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed5f-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4ed5f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed5f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ed5f-141">INPUTS</span></span>

### <span data-ttu-id="4ed5f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4ed5f-142">System.String</span></span>

## <span data-ttu-id="4ed5f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ed5f-143">OUTPUTS</span></span>

### <span data-ttu-id="4ed5f-144">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="4ed5f-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="4ed5f-145">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4ed5f-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4ed5f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ed5f-146">NOTES</span></span>

## <span data-ttu-id="4ed5f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ed5f-147">RELATED LINKS</span></span>

[<span data-ttu-id="4ed5f-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ed5f-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4ed5f-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ed5f-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="4ed5f-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ed5f-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="4ed5f-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ed5f-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="4ed5f-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ed5f-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="4ed5f-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ed5f-153">Update-AzVM</span></span>](./Update-AzVM.md)


