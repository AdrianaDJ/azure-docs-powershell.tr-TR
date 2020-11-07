---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 7e7b32322d6c6a131ee906c56b0c4fbdd0a5d63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759467"
---
# <span data-ttu-id="ffe04-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="ffe04-101">Update-AzReservation</span></span>

## <span data-ttu-id="ffe04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffe04-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe04-103">Güncelleştir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="ffe04-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="ffe04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffe04-104">SYNTAX</span></span>

### <span data-ttu-id="ffe04-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ffe04-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe04-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="ffe04-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffe04-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffe04-107">DESCRIPTION</span></span>
<span data-ttu-id="ffe04-108">Uygulamasının uygulanan kapsamlarını güncelleştirir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="ffe04-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="ffe04-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffe04-109">EXAMPLES</span></span>

### <span data-ttu-id="ffe04-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ffe04-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="ffe04-111">Belirtilen AppliedScopeType 'i `Reservation` tek ve ınstanceesnekliğini açık olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ffe04-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="ffe04-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ffe04-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="ffe04-113">AppliedScopeType, `Reservation` paylaşılan ve ınstanceesnekliği 'Nin kapalı olduğunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ffe04-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="ffe04-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffe04-114">PARAMETERS</span></span>

### <span data-ttu-id="ffe04-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="ffe04-115">-AppliedScope</span></span>
<span data-ttu-id="ffe04-116">`Reservation`Uygulanabilmesini sağlayan SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ffe04-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="ffe04-117">-AppliedScopeType</span></span>
<span data-ttu-id="ffe04-118">Uygulanan kapsamın türü</span><span class="sxs-lookup"><span data-stu-id="ffe04-118">Type of the Applied Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe04-119">-DefaultProfile</span></span>
<span data-ttu-id="ffe04-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ffe04-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffe04-121">-Instanceesnekliği</span><span class="sxs-lookup"><span data-stu-id="ffe04-121">-InstanceFlexibility</span></span>
<span data-ttu-id="ffe04-122">Varsa, uygulamasının ınstanceesnekliği değerini güncelleştirir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="ffe04-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="ffe04-123">Belirtilmezse, varolan değer değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="ffe04-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ffe04-124">-Name</span></span>
<span data-ttu-id="ffe04-125">Ayırma adı</span><span class="sxs-lookup"><span data-stu-id="ffe04-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-126">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="ffe04-126">-Reservation</span></span>
<span data-ttu-id="ffe04-127">İçin yöneltme nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ffe04-127">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-128">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="ffe04-128">-ReservationId</span></span>
<span data-ttu-id="ffe04-129">`Reservation`Güncelleştirilecek</span><span class="sxs-lookup"><span data-stu-id="ffe04-129">Id of the `Reservation` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-130">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="ffe04-130">-ReservationOrderId</span></span>
<span data-ttu-id="ffe04-131">`ReservationOrder`Güncelleştirilecek</span><span class="sxs-lookup"><span data-stu-id="ffe04-131">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffe04-132">-Confirm</span></span>
<span data-ttu-id="ffe04-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffe04-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffe04-134">-WhatIf</span></span>
<span data-ttu-id="ffe04-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffe04-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffe04-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffe04-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe04-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe04-137">CommonParameters</span></span>
<span data-ttu-id="ffe04-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffe04-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe04-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe04-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe04-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffe04-140">INPUTS</span></span>

### <span data-ttu-id="ffe04-141">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="ffe04-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ffe04-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffe04-142">OUTPUTS</span></span>

### <span data-ttu-id="ffe04-143">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="ffe04-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ffe04-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffe04-144">NOTES</span></span>

## <span data-ttu-id="ffe04-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffe04-145">RELATED LINKS</span></span>