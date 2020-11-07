---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936924"
---
# <span data-ttu-id="7008b-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="7008b-101">Remove-AzVM</span></span>

## <span data-ttu-id="7008b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7008b-102">SYNOPSIS</span></span>
<span data-ttu-id="7008b-103">Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7008b-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="7008b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7008b-104">SYNTAX</span></span>

### <span data-ttu-id="7008b-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7008b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7008b-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="7008b-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7008b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7008b-107">DESCRIPTION</span></span>
<span data-ttu-id="7008b-108">**Remove-AzVM** cmdlet 'i Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7008b-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="7008b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7008b-109">EXAMPLES</span></span>

### <span data-ttu-id="7008b-110">Örnek 1: sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="7008b-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7008b-111">Bu komut, kaynak grubundaki VirtualMachine07 adındaki sanal makineyi kaldırır ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7008b-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="7008b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7008b-112">PARAMETERS</span></span>

### <span data-ttu-id="7008b-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="7008b-113">-AsJob</span></span>
<span data-ttu-id="7008b-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="7008b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7008b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7008b-115">-DefaultProfile</span></span>
<span data-ttu-id="7008b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7008b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7008b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7008b-117">-Force</span></span>
<span data-ttu-id="7008b-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7008b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7008b-119">-ID</span><span class="sxs-lookup"><span data-stu-id="7008b-119">-Id</span></span>
<span data-ttu-id="7008b-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7008b-120">The resource group name.</span></span>

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

### <span data-ttu-id="7008b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7008b-121">-Name</span></span>
<span data-ttu-id="7008b-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7008b-122">The resource name.</span></span>

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

### <span data-ttu-id="7008b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7008b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7008b-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7008b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7008b-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="7008b-125">-Confirm</span></span>
<span data-ttu-id="7008b-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7008b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7008b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7008b-127">-WhatIf</span></span>
<span data-ttu-id="7008b-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7008b-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7008b-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7008b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7008b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7008b-130">CommonParameters</span></span>
<span data-ttu-id="7008b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7008b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7008b-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7008b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7008b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7008b-133">INPUTS</span></span>

### <span data-ttu-id="7008b-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7008b-134">None</span></span>
<span data-ttu-id="7008b-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7008b-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7008b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7008b-136">OUTPUTS</span></span>

### <span data-ttu-id="7008b-137">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7008b-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="7008b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7008b-138">NOTES</span></span>

## <span data-ttu-id="7008b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7008b-139">RELATED LINKS</span></span>

[<span data-ttu-id="7008b-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7008b-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7008b-141">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7008b-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7008b-142">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="7008b-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="7008b-143">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="7008b-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7008b-144">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="7008b-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="7008b-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7008b-145">Update-AzVM</span></span>](./Update-AzVM.md)


