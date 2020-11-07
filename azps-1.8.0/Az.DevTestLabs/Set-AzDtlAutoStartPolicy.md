---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: c751335f05f0e6ac9df5acb585dc5eb651d957a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760943"
---
# <span data-ttu-id="47e31-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="47e31-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="47e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e31-102">SYNOPSIS</span></span>
<span data-ttu-id="47e31-103">DevTest laboratuvarlarında laboratuarın otomatik başlatma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="47e31-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="47e31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47e31-104">SYNTAX</span></span>

### <span data-ttu-id="47e31-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47e31-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47e31-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="47e31-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47e31-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="47e31-107">DESCRIPTION</span></span>
<span data-ttu-id="47e31-108">**Set-AzDtlAutoStartPolicy** cmdlet 'i, laboratuarın otomatik başlatma ilkesini ayarlar ve laboratuvar sanal makinelerinin otomatik başlatma için zamanlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="47e31-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="47e31-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="47e31-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="47e31-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47e31-110">EXAMPLES</span></span>

## <span data-ttu-id="47e31-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47e31-111">PARAMETERS</span></span>

### <span data-ttu-id="47e31-112">-Gün</span><span class="sxs-lookup"><span data-stu-id="47e31-112">-Days</span></span>
<span data-ttu-id="47e31-113">Laboratuarın sanal makinelerinin başlatılması gerektiğinde, hafta olarak bir dizi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="47e31-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e31-114">-DefaultProfile</span></span>
<span data-ttu-id="47e31-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="47e31-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47e31-116">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="47e31-116">-Disable</span></span>
<span data-ttu-id="47e31-117">Bu cmdlet 'in laboratuarda sanal makinelerin ilkesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47e31-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="47e31-118">-Enable</span><span class="sxs-lookup"><span data-stu-id="47e31-118">-Enable</span></span>
<span data-ttu-id="47e31-119">Bu cmdlet 'in laboratuarda sanal makinelerin ilkesini etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="47e31-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="47e31-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="47e31-120">-LabName</span></span>
<span data-ttu-id="47e31-121">Bu cmdlet 'in otomatik başlangıç ilkesini ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47e31-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="47e31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e31-122">-ResourceGroupName</span></span>
<span data-ttu-id="47e31-123">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47e31-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="47e31-124">Defalık</span><span class="sxs-lookup"><span data-stu-id="47e31-124">-Time</span></span>
<span data-ttu-id="47e31-125">Laboratuarın sanal makinelerinin başlatılması gereken zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="47e31-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="47e31-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="47e31-126">-Confirm</span></span>
<span data-ttu-id="47e31-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47e31-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e31-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e31-128">-WhatIf</span></span>
<span data-ttu-id="47e31-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47e31-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e31-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47e31-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e31-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e31-131">CommonParameters</span></span>
<span data-ttu-id="47e31-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47e31-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e31-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e31-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e31-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47e31-134">INPUTS</span></span>

### <span data-ttu-id="47e31-135">System. String</span><span class="sxs-lookup"><span data-stu-id="47e31-135">System.String</span></span>

## <span data-ttu-id="47e31-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47e31-136">OUTPUTS</span></span>

### <span data-ttu-id="47e31-137">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="47e31-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="47e31-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47e31-138">NOTES</span></span>

## <span data-ttu-id="47e31-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47e31-139">RELATED LINKS</span></span>

[<span data-ttu-id="47e31-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="47e31-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)


