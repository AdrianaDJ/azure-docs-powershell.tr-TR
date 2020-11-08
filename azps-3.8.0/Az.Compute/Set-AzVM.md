---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: c9b7ce0c55ff917839ff8047454dcced42653b3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096397"
---
# <span data-ttu-id="9a077-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="9a077-101">Set-AzVM</span></span>

## <span data-ttu-id="9a077-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a077-102">SYNOPSIS</span></span>
<span data-ttu-id="9a077-103">Sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="9a077-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="9a077-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a077-104">SYNTAX</span></span>

### <span data-ttu-id="9a077-105">GeneralizeResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9a077-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a077-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9a077-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a077-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9a077-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a077-108">Genelizevseçparametrekümesiadı</span><span class="sxs-lookup"><span data-stu-id="9a077-108">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a077-109">Redeployıdparametersetname</span><span class="sxs-lookup"><span data-stu-id="9a077-109">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a077-110">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9a077-110">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a077-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a077-111">DESCRIPTION</span></span>
<span data-ttu-id="9a077-112">**Set-AzVM** cmdlet 'i bir sanal makineyi genellerle işaretler.</span><span class="sxs-lookup"><span data-stu-id="9a077-112">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="9a077-113">Bu cmdlet 'i çalıştırmadan önce sanal makinede oturum açın ve Sysprep kullanarak sabit diski hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="9a077-113">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="9a077-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a077-114">EXAMPLES</span></span>

### <span data-ttu-id="9a077-115">Örnek 1: sanal makineyi Genelleştirilmiş olarak Işaretleme</span><span class="sxs-lookup"><span data-stu-id="9a077-115">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="9a077-116">Bu komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="9a077-116">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="9a077-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a077-117">PARAMETERS</span></span>

### <span data-ttu-id="9a077-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="9a077-118">-AsJob</span></span>
<span data-ttu-id="9a077-119">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="9a077-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9a077-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a077-120">-DefaultProfile</span></span>
<span data-ttu-id="9a077-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9a077-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a077-122">-Genelleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="9a077-122">-Generalized</span></span>
<span data-ttu-id="9a077-123">Bu cmdlet 'in bir sanal makineyi genellerle işaretdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a077-123">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a077-124">-ID</span><span class="sxs-lookup"><span data-stu-id="9a077-124">-Id</span></span>
<span data-ttu-id="9a077-125">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a077-125">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a077-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9a077-126">-Name</span></span>
<span data-ttu-id="9a077-127">Bu cmdlet 'in üzerinde çalıştırıldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a077-127">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a077-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9a077-128">-NoWait</span></span>
<span data-ttu-id="9a077-129">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="9a077-129">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9a077-130">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="9a077-130">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a077-131">-Yeniden uygulama</span><span class="sxs-lookup"><span data-stu-id="9a077-131">-Reapply</span></span>
<span data-ttu-id="9a077-132">Sanal makineyi yeniden uygulayın.</span><span class="sxs-lookup"><span data-stu-id="9a077-132">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a077-133">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="9a077-133">-Redeploy</span></span>
<span data-ttu-id="9a077-134">Bu cmdlet 'in herhangi bir sorunu çözmek için sanal makineyi farklı bir Azure ana bilgisayarına el ile yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a077-134">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="9a077-135">Bir sanal makineyi yeniden kullanıyorsanız, bu, kısa ömürlü sürücü verilerinin kaybedilmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="9a077-135">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a077-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a077-136">-ResourceGroupName</span></span>
<span data-ttu-id="9a077-137">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a077-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a077-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a077-138">CommonParameters</span></span>
<span data-ttu-id="9a077-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a077-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a077-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9a077-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a077-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a077-141">INPUTS</span></span>

### <span data-ttu-id="9a077-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9a077-142">System.String</span></span>

## <span data-ttu-id="9a077-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a077-143">OUTPUTS</span></span>

### <span data-ttu-id="9a077-144">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9a077-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="9a077-145">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9a077-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9a077-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a077-146">NOTES</span></span>

## <span data-ttu-id="9a077-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a077-147">RELATED LINKS</span></span>

[<span data-ttu-id="9a077-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9a077-148">Get-AzVM</span></span>](./Get-AzVM.md)

