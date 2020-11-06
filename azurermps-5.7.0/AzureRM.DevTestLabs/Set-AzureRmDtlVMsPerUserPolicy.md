---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 459ae0e3d18056c6579d4fd6248548155e1471cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589796"
---
# <span data-ttu-id="6a920-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="6a920-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="6a920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a920-102">SYNOPSIS</span></span>
<span data-ttu-id="6a920-103">DevTest laboratuvarlarında bir laboratuvarda Kullanıcı başına sanal makine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6a920-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a920-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a920-104">SYNTAX</span></span>

### <span data-ttu-id="6a920-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a920-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a920-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="6a920-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a920-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a920-107">DESCRIPTION</span></span>
<span data-ttu-id="6a920-108">**Set-AzureRmDtlVMsPerUserPolicy** cmdlet 'i, bir laboratuarın Kullanıcı başına sanal makine sayısını ayarlar; Kullanıcı başına izin verilen en fazla sanal makine sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6a920-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="6a920-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="6a920-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="6a920-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a920-110">EXAMPLES</span></span>

## <span data-ttu-id="6a920-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a920-111">PARAMETERS</span></span>

### <span data-ttu-id="6a920-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a920-112">-DefaultProfile</span></span>
<span data-ttu-id="6a920-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6a920-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a920-114">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="6a920-114">-Disable</span></span>
<span data-ttu-id="6a920-115">Bu cmdlet 'in laboratuar ilkesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a920-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a920-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="6a920-116">-Enable</span></span>
<span data-ttu-id="6a920-117">Bu cmdlet 'in laboratuvar için ilke etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a920-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a920-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="6a920-118">-LabName</span></span>
<span data-ttu-id="6a920-119">Bu cmdlet 'in Kullanıcı başına sanal makineleri ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a920-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a920-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="6a920-120">-MaxVMs</span></span>
<span data-ttu-id="6a920-121">Laboratuvarda oluşturulabilecek en fazla sanal makine sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a920-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a920-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a920-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a920-123">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a920-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="6a920-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a920-124">-Confirm</span></span>
<span data-ttu-id="6a920-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a920-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a920-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a920-126">-WhatIf</span></span>
<span data-ttu-id="6a920-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a920-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a920-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a920-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a920-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a920-129">CommonParameters</span></span>
<span data-ttu-id="6a920-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a920-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a920-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a920-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a920-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a920-132">INPUTS</span></span>

### <span data-ttu-id="6a920-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6a920-133">None</span></span>
<span data-ttu-id="6a920-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6a920-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a920-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a920-135">OUTPUTS</span></span>

### <span data-ttu-id="6a920-136">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="6a920-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="6a920-137">Bu cmdlet, laboratuarda bir kullanıcı tarafından oluşturulabilen en fazla sanal makine sayısını belirten ilkeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="6a920-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="6a920-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a920-138">NOTES</span></span>

## <span data-ttu-id="6a920-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a920-139">RELATED LINKS</span></span>

[<span data-ttu-id="6a920-140">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="6a920-140">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


