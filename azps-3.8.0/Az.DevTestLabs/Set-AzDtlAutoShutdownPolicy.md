---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b8c6965034b741ddd281bb81c9748a25d7038be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097864"
---
# <span data-ttu-id="701c4-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="701c4-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="701c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="701c4-102">SYNOPSIS</span></span>
<span data-ttu-id="701c4-103">Laboratuvar dev-test laboratuarının otomatik kapatma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="701c4-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="701c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="701c4-104">SYNTAX</span></span>

### <span data-ttu-id="701c4-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="701c4-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="701c4-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="701c4-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="701c4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="701c4-107">DESCRIPTION</span></span>
<span data-ttu-id="701c4-108">**Set-AzDtlAutoShutdownPolicy** cmdlet 'i, belirli bir zamanda laboratuarda tüm sanal makineleri otomatik olarak kapatan bir laboratuvarın otomatik kapatma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="701c4-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="701c4-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="701c4-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="701c4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="701c4-110">EXAMPLES</span></span>

## <span data-ttu-id="701c4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="701c4-111">PARAMETERS</span></span>

### <span data-ttu-id="701c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="701c4-112">-DefaultProfile</span></span>
<span data-ttu-id="701c4-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="701c4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="701c4-114">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="701c4-114">-Disable</span></span>
<span data-ttu-id="701c4-115">Cmdlet 'teki ilkeyi devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="701c4-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="701c4-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="701c4-116">-Enable</span></span>
<span data-ttu-id="701c4-117">Cmdlet 'teki ilkeyi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="701c4-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="701c4-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="701c4-118">-LabName</span></span>
<span data-ttu-id="701c4-119">Bu cmdlet 'in otomatik kapatma ilkesini ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="701c4-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="701c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="701c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="701c4-121">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="701c4-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="701c4-122">Defalık</span><span class="sxs-lookup"><span data-stu-id="701c4-122">-Time</span></span>
<span data-ttu-id="701c4-123">Laboratuarın laboratuvarındaki sanal makinelerin kapatılması gereken zamanı için **Tarih saat** değeri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="701c4-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="701c4-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="701c4-124">-Confirm</span></span>
<span data-ttu-id="701c4-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="701c4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="701c4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="701c4-126">-WhatIf</span></span>
<span data-ttu-id="701c4-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="701c4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="701c4-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="701c4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="701c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="701c4-129">CommonParameters</span></span>
<span data-ttu-id="701c4-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="701c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="701c4-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="701c4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="701c4-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="701c4-132">INPUTS</span></span>

### <span data-ttu-id="701c4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="701c4-133">System.String</span></span>

## <span data-ttu-id="701c4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="701c4-134">OUTPUTS</span></span>

### <span data-ttu-id="701c4-135">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="701c4-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="701c4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="701c4-136">NOTES</span></span>

## <span data-ttu-id="701c4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="701c4-137">RELATED LINKS</span></span>

[<span data-ttu-id="701c4-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="701c4-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


