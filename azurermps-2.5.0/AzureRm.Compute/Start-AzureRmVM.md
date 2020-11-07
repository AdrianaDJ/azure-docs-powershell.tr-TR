---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939564"
---
# <span data-ttu-id="f2cb2-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2cb2-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="f2cb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cb2-103">Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2cb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2cb2-104">SYNTAX</span></span>

### <span data-ttu-id="f2cb2-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2cb2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2cb2-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="f2cb2-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2cb2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2cb2-107">DESCRIPTION</span></span>
<span data-ttu-id="f2cb2-108">**Start-AzureRmVM** cmdlet 'ı bir Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f2cb2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2cb2-109">EXAMPLES</span></span>

### <span data-ttu-id="f2cb2-110">Örnek 1: sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="f2cb2-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f2cb2-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f2cb2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2cb2-112">PARAMETERS</span></span>

### <span data-ttu-id="f2cb2-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="f2cb2-113">-AsJob</span></span>
<span data-ttu-id="f2cb2-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f2cb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2cb2-115">-DefaultProfile</span></span>
<span data-ttu-id="f2cb2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2cb2-117">-ID</span><span class="sxs-lookup"><span data-stu-id="f2cb2-117">-Id</span></span>
<span data-ttu-id="f2cb2-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-118">The resource group name.</span></span>

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

### <span data-ttu-id="f2cb2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2cb2-119">-Name</span></span>
<span data-ttu-id="f2cb2-120">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="f2cb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="f2cb2-122">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f2cb2-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2cb2-123">-Confirm</span></span>
<span data-ttu-id="f2cb2-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2cb2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2cb2-125">-WhatIf</span></span>
<span data-ttu-id="f2cb2-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2cb2-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2cb2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cb2-128">CommonParameters</span></span>
<span data-ttu-id="f2cb2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cb2-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2cb2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cb2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2cb2-131">INPUTS</span></span>

### <span data-ttu-id="f2cb2-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f2cb2-132">None</span></span>
<span data-ttu-id="f2cb2-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f2cb2-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2cb2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2cb2-134">OUTPUTS</span></span>

### <span data-ttu-id="f2cb2-135">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f2cb2-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f2cb2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2cb2-136">NOTES</span></span>

## <span data-ttu-id="f2cb2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2cb2-137">RELATED LINKS</span></span>

[<span data-ttu-id="f2cb2-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2cb2-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f2cb2-139">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2cb2-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="f2cb2-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2cb2-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="f2cb2-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2cb2-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="f2cb2-142">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2cb2-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="f2cb2-143">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2cb2-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


