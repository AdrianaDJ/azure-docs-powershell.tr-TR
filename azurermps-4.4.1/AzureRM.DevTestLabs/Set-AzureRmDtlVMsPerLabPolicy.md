---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 95908e6b0976baf2ce9f3c117f54a6f1552e4957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763736"
---
# <span data-ttu-id="5cd3c-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd3c-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="5cd3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd3c-103">DevTest laboratuvarlarında bir laboratuarın laboratuar ilkesi başına sanal makine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cd3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cd3c-104">SYNTAX</span></span>

### <span data-ttu-id="5cd3c-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cd3c-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cd3c-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="5cd3c-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd3c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cd3c-107">DESCRIPTION</span></span>
<span data-ttu-id="5cd3c-108">**Set-AzureRmDtlVMsPerLabPolicy** cmdlet 'i laboratuarda gelen sanal makineleri bir laboratuvarda izin verilen toplam sanal makine sayısını ayarlayan bir laboratuvar ilkesi başına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="5cd3c-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="5cd3c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cd3c-110">EXAMPLES</span></span>

## <span data-ttu-id="5cd3c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cd3c-111">PARAMETERS</span></span>

### <span data-ttu-id="5cd3c-112">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="5cd3c-112">-Disable</span></span>
<span data-ttu-id="5cd3c-113">Bu cmdlet 'in laboratuar ilkesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-113">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="5cd3c-114">-Enable</span><span class="sxs-lookup"><span data-stu-id="5cd3c-114">-Enable</span></span>
<span data-ttu-id="5cd3c-115">Bu cmdlet 'in laboratuar ilkesini etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-115">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="5cd3c-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="5cd3c-116">-LabName</span></span>
<span data-ttu-id="5cd3c-117">Bu cmdlet 'in sanal makineleri laboratuar ilkesi başına ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="5cd3c-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="5cd3c-118">-MaxVMs</span></span>
<span data-ttu-id="5cd3c-119">Laboratuvarda oluşturulabilecek en fazla sanal makine sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="5cd3c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd3c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5cd3c-121">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5cd3c-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cd3c-122">-Confirm</span></span>
<span data-ttu-id="5cd3c-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd3c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd3c-124">-WhatIf</span></span>
<span data-ttu-id="5cd3c-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd3c-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd3c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd3c-127">-DefaultProfile</span></span>
<span data-ttu-id="5cd3c-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd3c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd3c-129">CommonParameters</span></span>
<span data-ttu-id="5cd3c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd3c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd3c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd3c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cd3c-132">INPUTS</span></span>

## <span data-ttu-id="5cd3c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cd3c-133">OUTPUTS</span></span>

### <span data-ttu-id="5cd3c-134">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd3c-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="5cd3c-135">Bu cmdlet, laboratuvarda oluşturulabilecek en fazla sanal makine sayısını belirten ilkeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5cd3c-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="5cd3c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cd3c-136">NOTES</span></span>

## <span data-ttu-id="5cd3c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cd3c-137">RELATED LINKS</span></span>

[<span data-ttu-id="5cd3c-138">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd3c-138">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


