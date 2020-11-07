---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: a147565a61bc75d71083c69766138c3a5a4659db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917251"
---
# <span data-ttu-id="1c706-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="1c706-101">Set-AzVM</span></span>

## <span data-ttu-id="1c706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c706-102">SYNOPSIS</span></span>
<span data-ttu-id="1c706-103">Sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="1c706-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="1c706-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c706-104">SYNTAX</span></span>

### <span data-ttu-id="1c706-105">GeneralizeResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c706-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c706-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1c706-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c706-107">Genelizevseçparametrekümesiadı</span><span class="sxs-lookup"><span data-stu-id="1c706-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c706-108">Redeployıdparametersetname</span><span class="sxs-lookup"><span data-stu-id="1c706-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c706-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c706-109">DESCRIPTION</span></span>
<span data-ttu-id="1c706-110">**Set-AzVM** cmdlet 'i bir sanal makineyi genellerle işaretler.</span><span class="sxs-lookup"><span data-stu-id="1c706-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="1c706-111">Bu cmdlet 'i çalıştırmadan önce sanal makinede oturum açın ve Sysprep kullanarak sabit diski hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="1c706-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="1c706-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c706-112">EXAMPLES</span></span>

### <span data-ttu-id="1c706-113">Örnek 1: sanal makineyi Genelleştirilmiş olarak Işaretleme</span><span class="sxs-lookup"><span data-stu-id="1c706-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="1c706-114">Bu komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="1c706-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="1c706-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c706-115">PARAMETERS</span></span>

### <span data-ttu-id="1c706-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="1c706-116">-AsJob</span></span>
<span data-ttu-id="1c706-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="1c706-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1c706-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c706-118">-DefaultProfile</span></span>
<span data-ttu-id="1c706-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c706-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c706-120">-Genelleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="1c706-120">-Generalized</span></span>
<span data-ttu-id="1c706-121">Bu cmdlet 'in bir sanal makineyi genellerle işaretdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c706-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="1c706-122">-ID</span><span class="sxs-lookup"><span data-stu-id="1c706-122">-Id</span></span>
<span data-ttu-id="1c706-123">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c706-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c706-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c706-124">-Name</span></span>
<span data-ttu-id="1c706-125">Bu cmdlet 'in üzerinde çalıştırıldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c706-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c706-126">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="1c706-126">-Redeploy</span></span>
<span data-ttu-id="1c706-127">Bu cmdlet 'in herhangi bir sorunu çözmek için sanal makineyi farklı bir Azure ana bilgisayarına el ile yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c706-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="1c706-128">Bir sanal makineyi yeniden kullanıyorsanız, bu, kısa ömürlü sürücü verilerinin kaybedilmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="1c706-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="1c706-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c706-129">-ResourceGroupName</span></span>
<span data-ttu-id="1c706-130">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c706-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c706-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c706-131">CommonParameters</span></span>
<span data-ttu-id="1c706-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c706-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c706-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c706-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c706-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c706-134">INPUTS</span></span>

### <span data-ttu-id="1c706-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1c706-135">System.String</span></span>

## <span data-ttu-id="1c706-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c706-136">OUTPUTS</span></span>

### <span data-ttu-id="1c706-137">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="1c706-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="1c706-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c706-138">NOTES</span></span>

## <span data-ttu-id="1c706-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c706-139">RELATED LINKS</span></span>

[<span data-ttu-id="1c706-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1c706-140">Get-AzVM</span></span>](./Get-AzVM.md)


