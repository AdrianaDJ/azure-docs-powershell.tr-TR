---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095879"
---
# <span data-ttu-id="92a9b-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="92a9b-101">Update-AzReservation</span></span>

## <span data-ttu-id="92a9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="92a9b-103">Güncelleştir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="92a9b-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="92a9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92a9b-104">SYNTAX</span></span>

### <span data-ttu-id="92a9b-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="92a9b-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a9b-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="92a9b-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92a9b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="92a9b-107">DESCRIPTION</span></span>
<span data-ttu-id="92a9b-108">Uygulamasının uygulanan kapsamlarını güncelleştirir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="92a9b-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="92a9b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92a9b-109">EXAMPLES</span></span>

### <span data-ttu-id="92a9b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="92a9b-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="92a9b-111">Belirtilen AppliedScopeType 'i `Reservation` tek ve ınstanceesnekliğini açık olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="92a9b-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="92a9b-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="92a9b-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="92a9b-113">AppliedScopeType, `Reservation` paylaşılan ve ınstanceesnekliği 'Nin kapalı olduğunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="92a9b-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="92a9b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92a9b-114">PARAMETERS</span></span>

### <span data-ttu-id="92a9b-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="92a9b-115">-AppliedScope</span></span>
<span data-ttu-id="92a9b-116">`Reservation`Uygulanabilmesini sağlayan SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="92a9b-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="92a9b-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="92a9b-117">-AppliedScopeType</span></span>
<span data-ttu-id="92a9b-118">Uygulanan kapsamın türü</span><span class="sxs-lookup"><span data-stu-id="92a9b-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="92a9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a9b-119">-DefaultProfile</span></span>
<span data-ttu-id="92a9b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92a9b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92a9b-121">-Instanceesnekliği</span><span class="sxs-lookup"><span data-stu-id="92a9b-121">-InstanceFlexibility</span></span>
<span data-ttu-id="92a9b-122">Varsa, uygulamasının ınstanceesnekliği değerini güncelleştirir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="92a9b-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="92a9b-123">Belirtilmezse, varolan değer değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="92a9b-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="92a9b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="92a9b-124">-Name</span></span>
<span data-ttu-id="92a9b-125">Ayırma adı</span><span class="sxs-lookup"><span data-stu-id="92a9b-125">Name of Reservation</span></span>

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

### <span data-ttu-id="92a9b-126">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="92a9b-126">-Reservation</span></span>
<span data-ttu-id="92a9b-127">İçin yöneltme nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="92a9b-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="92a9b-128">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="92a9b-128">-ReservationId</span></span>
<span data-ttu-id="92a9b-129">`Reservation`Güncelleştirilecek</span><span class="sxs-lookup"><span data-stu-id="92a9b-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="92a9b-130">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="92a9b-130">-ReservationOrderId</span></span>
<span data-ttu-id="92a9b-131">`ReservationOrder`Güncelleştirilecek</span><span class="sxs-lookup"><span data-stu-id="92a9b-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="92a9b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="92a9b-132">-Confirm</span></span>
<span data-ttu-id="92a9b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92a9b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a9b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a9b-134">-WhatIf</span></span>
<span data-ttu-id="92a9b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92a9b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92a9b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92a9b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a9b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a9b-137">CommonParameters</span></span>
<span data-ttu-id="92a9b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92a9b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a9b-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="92a9b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a9b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92a9b-140">INPUTS</span></span>

### <span data-ttu-id="92a9b-141">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="92a9b-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="92a9b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92a9b-142">OUTPUTS</span></span>

### <span data-ttu-id="92a9b-143">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="92a9b-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="92a9b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92a9b-144">NOTES</span></span>

## <span data-ttu-id="92a9b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92a9b-145">RELATED LINKS</span></span>
