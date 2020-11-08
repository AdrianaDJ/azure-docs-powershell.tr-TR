---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275537"
---
# <span data-ttu-id="8af0b-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8af0b-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="8af0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8af0b-102">SYNOPSIS</span></span>
<span data-ttu-id="8af0b-103">DevTest laboratuvarlarında bir laboratuvarda Kullanıcı başına sanal makine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8af0b-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="8af0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8af0b-104">SYNTAX</span></span>

### <span data-ttu-id="8af0b-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8af0b-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af0b-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="8af0b-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af0b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8af0b-107">DESCRIPTION</span></span>
<span data-ttu-id="8af0b-108">**Set-AzDtlVMsPerUserPolicy** cmdlet 'i, bir laboratuarın Kullanıcı başına sanal makine sayısını ayarlar; Kullanıcı başına izin verilen en fazla sanal makine sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8af0b-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="8af0b-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="8af0b-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="8af0b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8af0b-110">EXAMPLES</span></span>

## <span data-ttu-id="8af0b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8af0b-111">PARAMETERS</span></span>

### <span data-ttu-id="8af0b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af0b-112">-DefaultProfile</span></span>
<span data-ttu-id="8af0b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8af0b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8af0b-114">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="8af0b-114">-Disable</span></span>
<span data-ttu-id="8af0b-115">Bu cmdlet 'in laboratuar ilkesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8af0b-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="8af0b-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="8af0b-116">-Enable</span></span>
<span data-ttu-id="8af0b-117">Bu cmdlet 'in laboratuvar için ilke etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8af0b-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="8af0b-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="8af0b-118">-LabName</span></span>
<span data-ttu-id="8af0b-119">Bu cmdlet 'in Kullanıcı başına sanal makineleri ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8af0b-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="8af0b-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="8af0b-120">-MaxVMs</span></span>
<span data-ttu-id="8af0b-121">Laboratuvarda oluşturulabilecek en fazla sanal makine sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8af0b-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="8af0b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af0b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8af0b-123">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8af0b-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="8af0b-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="8af0b-124">-Confirm</span></span>
<span data-ttu-id="8af0b-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8af0b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af0b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af0b-126">-WhatIf</span></span>
<span data-ttu-id="8af0b-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8af0b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af0b-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8af0b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af0b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af0b-129">CommonParameters</span></span>
<span data-ttu-id="8af0b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8af0b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af0b-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af0b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af0b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8af0b-132">INPUTS</span></span>

### <span data-ttu-id="8af0b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8af0b-133">System.String</span></span>

## <span data-ttu-id="8af0b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8af0b-134">OUTPUTS</span></span>

### <span data-ttu-id="8af0b-135">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8af0b-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="8af0b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8af0b-136">NOTES</span></span>

## <span data-ttu-id="8af0b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8af0b-137">RELATED LINKS</span></span>

[<span data-ttu-id="8af0b-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8af0b-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


