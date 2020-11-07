---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 6cf37c453d47278958ccd84eaf817e6dc118b16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762654"
---
# <span data-ttu-id="5a880-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a880-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="5a880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a880-102">SYNOPSIS</span></span>
<span data-ttu-id="5a880-103">Bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="5a880-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a880-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a880-104">SYNTAX</span></span>

### <span data-ttu-id="5a880-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a880-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a880-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="5a880-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a880-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a880-107">DESCRIPTION</span></span>
<span data-ttu-id="5a880-108">**Stop-AzureRmVM** cmdlet 'ı bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="5a880-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="5a880-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a880-109">EXAMPLES</span></span>

### <span data-ttu-id="5a880-110">Örnek 1: sanal makineyi durdurma</span><span class="sxs-lookup"><span data-stu-id="5a880-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="5a880-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="5a880-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="5a880-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a880-112">PARAMETERS</span></span>

### <span data-ttu-id="5a880-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5a880-113">-AsJob</span></span>
<span data-ttu-id="5a880-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="5a880-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5a880-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a880-115">-DefaultProfile</span></span>
<span data-ttu-id="5a880-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a880-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a880-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5a880-117">-Force</span></span>
<span data-ttu-id="5a880-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5a880-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a880-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5a880-119">-Id</span></span>
<span data-ttu-id="5a880-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5a880-120">The resource group name.</span></span>

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

### <span data-ttu-id="5a880-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a880-121">-Name</span></span>
<span data-ttu-id="5a880-122">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="5a880-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="5a880-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a880-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a880-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a880-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5a880-125">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="5a880-125">-StayProvisioned</span></span>
<span data-ttu-id="5a880-126">Cmdlet, VMSS içindeki tüm sanal makineleri durdurur ancak bunları serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="5a880-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="5a880-127">Hesap, durdurulan sanal makineler için ücretlendirilecek.</span><span class="sxs-lookup"><span data-stu-id="5a880-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="5a880-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a880-128">-Confirm</span></span>
<span data-ttu-id="5a880-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a880-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a880-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a880-130">-WhatIf</span></span>
<span data-ttu-id="5a880-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a880-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a880-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a880-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a880-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a880-133">CommonParameters</span></span>
<span data-ttu-id="5a880-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a880-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a880-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a880-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a880-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a880-136">INPUTS</span></span>

### <span data-ttu-id="5a880-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5a880-137">None</span></span>
<span data-ttu-id="5a880-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5a880-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a880-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a880-139">OUTPUTS</span></span>

### <span data-ttu-id="5a880-140">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="5a880-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="5a880-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a880-141">NOTES</span></span>

## <span data-ttu-id="5a880-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a880-142">RELATED LINKS</span></span>

[<span data-ttu-id="5a880-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a880-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5a880-144">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a880-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="5a880-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a880-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5a880-146">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a880-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="5a880-147">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a880-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5a880-148">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a880-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

