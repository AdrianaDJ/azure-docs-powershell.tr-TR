---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764078"
---
# <span data-ttu-id="10bf8-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10bf8-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="10bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="10bf8-103">Sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="10bf8-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10bf8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10bf8-104">SYNTAX</span></span>

### <span data-ttu-id="10bf8-105">GeneralizeResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="10bf8-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10bf8-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="10bf8-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10bf8-107">Genelizevseçparametrekümesiadı</span><span class="sxs-lookup"><span data-stu-id="10bf8-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10bf8-108">Redeployıdparametersetname</span><span class="sxs-lookup"><span data-stu-id="10bf8-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10bf8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="10bf8-109">DESCRIPTION</span></span>
<span data-ttu-id="10bf8-110">**Set-AzureRmVM** cmdlet 'i bir sanal makineyi genellerle işaretler.</span><span class="sxs-lookup"><span data-stu-id="10bf8-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="10bf8-111">Bu cmdlet 'i çalıştırmadan önce sanal makinede oturum açın ve Sysprep kullanarak sabit diski hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="10bf8-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="10bf8-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10bf8-112">EXAMPLES</span></span>

### <span data-ttu-id="10bf8-113">Örnek 1: sanal makineyi Genelleştirilmiş olarak Işaretleme</span><span class="sxs-lookup"><span data-stu-id="10bf8-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="10bf8-114">Bu komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="10bf8-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="10bf8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10bf8-115">PARAMETERS</span></span>

### <span data-ttu-id="10bf8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bf8-116">-DefaultProfile</span></span>
<span data-ttu-id="10bf8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10bf8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10bf8-118">-Genelleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="10bf8-118">-Generalized</span></span>
<span data-ttu-id="10bf8-119">Bu cmdlet 'in bir sanal makineyi genellerle işaretdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10bf8-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bf8-120">-ID</span><span class="sxs-lookup"><span data-stu-id="10bf8-120">-Id</span></span>
<span data-ttu-id="10bf8-121">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="10bf8-121">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="10bf8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="10bf8-122">-Name</span></span>
<span data-ttu-id="10bf8-123">Bu cmdlet 'in üzerinde çalıştırıldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10bf8-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bf8-124">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="10bf8-124">-Redeploy</span></span>
<span data-ttu-id="10bf8-125">Bu cmdlet 'in herhangi bir sorunu çözmek için sanal makineyi farklı bir Azure ana bilgisayarına el ile yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10bf8-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="10bf8-126">Bir sanal makineyi yeniden kullanıyorsanız, bu, kısa ömürlü sürücü verilerinin kaybedilmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="10bf8-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bf8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bf8-127">-ResourceGroupName</span></span>
<span data-ttu-id="10bf8-128">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10bf8-128">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="10bf8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bf8-129">CommonParameters</span></span>
<span data-ttu-id="10bf8-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10bf8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bf8-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10bf8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bf8-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10bf8-132">INPUTS</span></span>

## <span data-ttu-id="10bf8-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10bf8-133">OUTPUTS</span></span>

## <span data-ttu-id="10bf8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10bf8-134">NOTES</span></span>

## <span data-ttu-id="10bf8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10bf8-135">RELATED LINKS</span></span>

[<span data-ttu-id="10bf8-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10bf8-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


