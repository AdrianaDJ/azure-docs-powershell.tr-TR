---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 000c9f2748bd1f80559d9fc80c206e4f1c9bf0c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763284"
---
# <span data-ttu-id="e90ea-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="e90ea-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="e90ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e90ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e90ea-103">DevTest laboratuvarlarında laboratuarın otomatik başlatma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e90ea-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e90ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e90ea-104">SYNTAX</span></span>

### <span data-ttu-id="e90ea-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e90ea-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e90ea-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="e90ea-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e90ea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e90ea-107">DESCRIPTION</span></span>
<span data-ttu-id="e90ea-108">**Set-AzureRmDtlAutoStartPolicy** cmdlet 'i, laboratuarın otomatik başlatma ilkesini ayarlar ve laboratuvar sanal makinelerinin otomatik başlatma için zamanlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e90ea-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="e90ea-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="e90ea-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="e90ea-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e90ea-110">EXAMPLES</span></span>

## <span data-ttu-id="e90ea-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e90ea-111">PARAMETERS</span></span>

### <span data-ttu-id="e90ea-112">-Gün</span><span class="sxs-lookup"><span data-stu-id="e90ea-112">-Days</span></span>
<span data-ttu-id="e90ea-113">Laboratuarın sanal makinelerinin başlatılması gerektiğinde, hafta olarak bir dizi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="e90ea-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90ea-114">-DefaultProfile</span></span>
<span data-ttu-id="e90ea-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e90ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e90ea-116">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="e90ea-116">-Disable</span></span>
<span data-ttu-id="e90ea-117">Bu cmdlet 'in laboratuarda sanal makinelerin ilkesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e90ea-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="e90ea-118">-Enable</span><span class="sxs-lookup"><span data-stu-id="e90ea-118">-Enable</span></span>
<span data-ttu-id="e90ea-119">Bu cmdlet 'in laboratuarda sanal makinelerin ilkesini etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e90ea-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="e90ea-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="e90ea-120">-LabName</span></span>
<span data-ttu-id="e90ea-121">Bu cmdlet 'in otomatik başlangıç ilkesini ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e90ea-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="e90ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="e90ea-123">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e90ea-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="e90ea-124">Defalık</span><span class="sxs-lookup"><span data-stu-id="e90ea-124">-Time</span></span>
<span data-ttu-id="e90ea-125">Laboratuarın sanal makinelerinin başlatılması gereken zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e90ea-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90ea-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="e90ea-126">-Confirm</span></span>
<span data-ttu-id="e90ea-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e90ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e90ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90ea-128">-WhatIf</span></span>
<span data-ttu-id="e90ea-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e90ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e90ea-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e90ea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e90ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90ea-131">CommonParameters</span></span>
<span data-ttu-id="e90ea-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e90ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90ea-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90ea-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90ea-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e90ea-134">INPUTS</span></span>

### <span data-ttu-id="e90ea-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e90ea-135">None</span></span>
<span data-ttu-id="e90ea-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e90ea-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e90ea-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e90ea-137">OUTPUTS</span></span>

### <span data-ttu-id="e90ea-138">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="e90ea-138">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="e90ea-139">Bu cmdlet, laboratuarın sanal makinelerinin başlatılması gereken ne zaman gerektiğini belirten zamanlamayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="e90ea-139">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="e90ea-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e90ea-140">NOTES</span></span>

## <span data-ttu-id="e90ea-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e90ea-141">RELATED LINKS</span></span>

[<span data-ttu-id="e90ea-142">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="e90ea-142">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


