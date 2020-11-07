---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935954"
---
# <span data-ttu-id="33af8-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="33af8-101">Stop-AzVM</span></span>

## <span data-ttu-id="33af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33af8-102">SYNOPSIS</span></span>
<span data-ttu-id="33af8-103">Bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="33af8-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="33af8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33af8-104">SYNTAX</span></span>

### <span data-ttu-id="33af8-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33af8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33af8-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="33af8-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33af8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="33af8-107">DESCRIPTION</span></span>
<span data-ttu-id="33af8-108">**Stop-AzVM** cmdlet 'ı bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="33af8-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="33af8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33af8-109">EXAMPLES</span></span>

### <span data-ttu-id="33af8-110">Örnek 1: sanal makineyi durdurma</span><span class="sxs-lookup"><span data-stu-id="33af8-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="33af8-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="33af8-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="33af8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33af8-112">PARAMETERS</span></span>

### <span data-ttu-id="33af8-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="33af8-113">-AsJob</span></span>
<span data-ttu-id="33af8-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="33af8-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33af8-115">-DefaultProfile</span></span>
<span data-ttu-id="33af8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33af8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33af8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="33af8-117">-Force</span></span>
<span data-ttu-id="33af8-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="33af8-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="33af8-119">-Id</span></span>
<span data-ttu-id="33af8-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="33af8-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="33af8-121">-Name</span></span>
<span data-ttu-id="33af8-122">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="33af8-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33af8-123">-ResourceGroupName</span></span>
<span data-ttu-id="33af8-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33af8-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-125">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="33af8-125">-StayProvisioned</span></span>
<span data-ttu-id="33af8-126">Cmdlet, VMSS içindeki tüm sanal makineleri durdurur ancak bunları serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="33af8-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="33af8-127">Hesap, durdurulan sanal makineler için ücretlendirilecek.</span><span class="sxs-lookup"><span data-stu-id="33af8-127">The account is charged for the stopped virtual machines.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="33af8-128">-Confirm</span></span>
<span data-ttu-id="33af8-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="33af8-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33af8-130">-WhatIf</span></span>
<span data-ttu-id="33af8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="33af8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33af8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="33af8-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33af8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33af8-133">CommonParameters</span></span>
<span data-ttu-id="33af8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33af8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33af8-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33af8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33af8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33af8-136">INPUTS</span></span>

### <span data-ttu-id="33af8-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33af8-137">None</span></span>
<span data-ttu-id="33af8-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="33af8-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33af8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33af8-139">OUTPUTS</span></span>

### <span data-ttu-id="33af8-140">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="33af8-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="33af8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33af8-141">NOTES</span></span>

## <span data-ttu-id="33af8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33af8-142">RELATED LINKS</span></span>

[<span data-ttu-id="33af8-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="33af8-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="33af8-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="33af8-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="33af8-145">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="33af8-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="33af8-146">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="33af8-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="33af8-147">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="33af8-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="33af8-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="33af8-148">Update-AzVM</span></span>](./Update-AzVM.md)


