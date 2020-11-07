---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: d1a3cf7a70810babd17f222a9a7a72c141f8ec6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752080"
---
# <span data-ttu-id="90fca-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="90fca-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="90fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90fca-102">SYNOPSIS</span></span>
<span data-ttu-id="90fca-103">DevTest laboratuvarlarında bir laboratuarın laboratuar ilkesi başına sanal makine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="90fca-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="90fca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90fca-104">SYNTAX</span></span>

### <span data-ttu-id="90fca-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90fca-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90fca-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="90fca-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90fca-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="90fca-107">DESCRIPTION</span></span>
<span data-ttu-id="90fca-108">**Set-AzDtlVMsPerLabPolicy** cmdlet 'i laboratuarda gelen sanal makineleri bir laboratuvarda izin verilen toplam sanal makine sayısını ayarlayan bir laboratuvar ilkesi başına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="90fca-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="90fca-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="90fca-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="90fca-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90fca-110">EXAMPLES</span></span>

## <span data-ttu-id="90fca-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90fca-111">PARAMETERS</span></span>

### <span data-ttu-id="90fca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90fca-112">-DefaultProfile</span></span>
<span data-ttu-id="90fca-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="90fca-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90fca-114">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="90fca-114">-Disable</span></span>
<span data-ttu-id="90fca-115">Bu cmdlet 'in laboratuar ilkesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90fca-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fca-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="90fca-116">-Enable</span></span>
<span data-ttu-id="90fca-117">Bu cmdlet 'in laboratuar ilkesini etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="90fca-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fca-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="90fca-118">-LabName</span></span>
<span data-ttu-id="90fca-119">Bu cmdlet 'in sanal makineleri laboratuar ilkesi başına ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90fca-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90fca-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="90fca-120">-MaxVMs</span></span>
<span data-ttu-id="90fca-121">Laboratuvarda oluşturulabilecek en fazla sanal makine sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90fca-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90fca-122">-ResourceGroupName</span></span>
<span data-ttu-id="90fca-123">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90fca-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="90fca-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="90fca-124">-Confirm</span></span>
<span data-ttu-id="90fca-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90fca-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fca-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90fca-126">-WhatIf</span></span>
<span data-ttu-id="90fca-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90fca-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90fca-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90fca-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90fca-129">CommonParameters</span></span>
<span data-ttu-id="90fca-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90fca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90fca-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90fca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90fca-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90fca-132">INPUTS</span></span>

### <span data-ttu-id="90fca-133">System. String</span><span class="sxs-lookup"><span data-stu-id="90fca-133">System.String</span></span>

## <span data-ttu-id="90fca-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90fca-134">OUTPUTS</span></span>

### <span data-ttu-id="90fca-135">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="90fca-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="90fca-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90fca-136">NOTES</span></span>

## <span data-ttu-id="90fca-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90fca-137">RELATED LINKS</span></span>

[<span data-ttu-id="90fca-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="90fca-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)

