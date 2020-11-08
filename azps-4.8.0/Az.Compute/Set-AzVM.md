---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268566"
---
# <span data-ttu-id="25d6a-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="25d6a-101">Set-AzVM</span></span>

## <span data-ttu-id="25d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="25d6a-103">Sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="25d6a-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="25d6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25d6a-104">SYNTAX</span></span>

### <span data-ttu-id="25d6a-105">GeneralizeResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25d6a-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d6a-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="25d6a-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d6a-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="25d6a-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d6a-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="25d6a-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d6a-109">Genelizevseçparametrekümesiadı</span><span class="sxs-lookup"><span data-stu-id="25d6a-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d6a-110">Redeployıdparametersetname</span><span class="sxs-lookup"><span data-stu-id="25d6a-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25d6a-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="25d6a-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25d6a-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="25d6a-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25d6a-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="25d6a-113">DESCRIPTION</span></span>
<span data-ttu-id="25d6a-114">**Set-AzVM** cmdlet 'i bir sanal makineyi genellerle işaretler.</span><span class="sxs-lookup"><span data-stu-id="25d6a-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="25d6a-115">Bu cmdlet 'i çalıştırmadan önce sanal makinede oturum açın ve Sysprep kullanarak sabit diski hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="25d6a-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25d6a-116">EXAMPLES</span></span>

### <span data-ttu-id="25d6a-117">Örnek 1: sanal makineyi Genelleştirilmiş olarak Işaretleme</span><span class="sxs-lookup"><span data-stu-id="25d6a-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="25d6a-118">Bu komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="25d6a-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="25d6a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25d6a-119">PARAMETERS</span></span>

### <span data-ttu-id="25d6a-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="25d6a-120">-AsJob</span></span>
<span data-ttu-id="25d6a-121">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="25d6a-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="25d6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d6a-122">-DefaultProfile</span></span>
<span data-ttu-id="25d6a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25d6a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25d6a-124">-Genelleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="25d6a-124">-Generalized</span></span>
<span data-ttu-id="25d6a-125">Bu cmdlet 'in bir sanal makineyi genellerle işaretdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d6a-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="25d6a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="25d6a-126">-Id</span></span>
<span data-ttu-id="25d6a-127">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d6a-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d6a-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="25d6a-128">-Name</span></span>
<span data-ttu-id="25d6a-129">Bu cmdlet 'in üzerinde çalıştırıldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d6a-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d6a-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="25d6a-130">-NoWait</span></span>
<span data-ttu-id="25d6a-131">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="25d6a-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="25d6a-132">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="25d6a-133">-Yeniden uygulama</span><span class="sxs-lookup"><span data-stu-id="25d6a-133">-Reapply</span></span>
<span data-ttu-id="25d6a-134">Sanal makineyi yeniden uygulayın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="25d6a-135">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="25d6a-135">-Redeploy</span></span>
<span data-ttu-id="25d6a-136">Bu cmdlet 'in herhangi bir sorunu çözmek için sanal makineyi farklı bir Azure ana bilgisayarına el ile yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25d6a-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="25d6a-137">Bir sanal makineyi yeniden kullanıyorsanız, bu, kısa ömürlü sürücü verilerinin kaybedilmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="25d6a-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="25d6a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d6a-138">-ResourceGroupName</span></span>
<span data-ttu-id="25d6a-139">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d6a-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d6a-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="25d6a-140">-SimulateEviction</span></span>
<span data-ttu-id="25d6a-141">Bu cmdlet 'in spot sanal makinenin çıkarmasına benzediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d6a-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="25d6a-142">Çıkarma işlemi, API 'YI çağırırken 30 dakika içinde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="25d6a-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d6a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d6a-143">CommonParameters</span></span>
<span data-ttu-id="25d6a-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25d6a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d6a-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d6a-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25d6a-146">INPUTS</span></span>

### <span data-ttu-id="25d6a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="25d6a-147">System.String</span></span>

## <span data-ttu-id="25d6a-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25d6a-148">OUTPUTS</span></span>

### <span data-ttu-id="25d6a-149">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="25d6a-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="25d6a-150">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="25d6a-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="25d6a-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25d6a-151">NOTES</span></span>

## <span data-ttu-id="25d6a-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25d6a-152">RELATED LINKS</span></span>

[<span data-ttu-id="25d6a-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="25d6a-153">Get-AzVM</span></span>](./Get-AzVM.md)


