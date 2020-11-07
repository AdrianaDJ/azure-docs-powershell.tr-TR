---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f694ef2985ecc983932b2ff78705be8a08315f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762161"
---
# <span data-ttu-id="b691e-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b691e-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="b691e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b691e-102">SYNOPSIS</span></span>
<span data-ttu-id="b691e-103">Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b691e-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b691e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b691e-104">SYNTAX</span></span>

### <span data-ttu-id="b691e-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b691e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b691e-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="b691e-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b691e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b691e-107">DESCRIPTION</span></span>
<span data-ttu-id="b691e-108">**Remove-AzureRmVM** cmdlet 'i Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b691e-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="b691e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b691e-109">EXAMPLES</span></span>

### <span data-ttu-id="b691e-110">Örnek 1: sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="b691e-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b691e-111">Bu komut, kaynak grubundaki VirtualMachine07 adındaki sanal makineyi kaldırır ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b691e-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="b691e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b691e-112">PARAMETERS</span></span>

### <span data-ttu-id="b691e-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="b691e-113">-AsJob</span></span>
<span data-ttu-id="b691e-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="b691e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b691e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b691e-115">-DefaultProfile</span></span>
<span data-ttu-id="b691e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b691e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b691e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b691e-117">-Force</span></span>
<span data-ttu-id="b691e-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b691e-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b691e-119">-ID</span><span class="sxs-lookup"><span data-stu-id="b691e-119">-Id</span></span>
<span data-ttu-id="b691e-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b691e-120">The resource group name.</span></span>

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

### <span data-ttu-id="b691e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="b691e-121">-Name</span></span>
<span data-ttu-id="b691e-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b691e-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b691e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b691e-123">-ResourceGroupName</span></span>
<span data-ttu-id="b691e-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b691e-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b691e-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b691e-125">-Confirm</span></span>
<span data-ttu-id="b691e-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b691e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b691e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b691e-127">-WhatIf</span></span>
<span data-ttu-id="b691e-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b691e-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b691e-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b691e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b691e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b691e-130">CommonParameters</span></span>
<span data-ttu-id="b691e-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b691e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b691e-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b691e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b691e-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b691e-133">INPUTS</span></span>

### <span data-ttu-id="b691e-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b691e-134">None</span></span>
<span data-ttu-id="b691e-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b691e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b691e-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b691e-136">OUTPUTS</span></span>

### <span data-ttu-id="b691e-137">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b691e-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="b691e-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b691e-138">NOTES</span></span>

## <span data-ttu-id="b691e-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b691e-139">RELATED LINKS</span></span>

[<span data-ttu-id="b691e-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b691e-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b691e-141">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b691e-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b691e-142">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b691e-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="b691e-143">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b691e-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b691e-144">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b691e-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b691e-145">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b691e-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


