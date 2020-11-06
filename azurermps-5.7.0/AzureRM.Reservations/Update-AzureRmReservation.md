---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589693"
---
# <span data-ttu-id="dd248-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="dd248-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="dd248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd248-102">SYNOPSIS</span></span>
<span data-ttu-id="dd248-103">Güncelleştir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="dd248-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd248-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd248-104">SYNTAX</span></span>

### <span data-ttu-id="dd248-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd248-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd248-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="dd248-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd248-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd248-107">DESCRIPTION</span></span>
<span data-ttu-id="dd248-108">Uygulamasının uygulanan kapsamlarını güncelleştirir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="dd248-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="dd248-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd248-109">EXAMPLES</span></span>

### <span data-ttu-id="dd248-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd248-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="dd248-111">Belirtilen ayırmanın AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="dd248-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="dd248-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dd248-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="dd248-113">Belirtilen ayırmanın AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="dd248-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="dd248-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd248-114">PARAMETERS</span></span>

### <span data-ttu-id="dd248-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="dd248-115">-AppliedScope</span></span>
<span data-ttu-id="dd248-116">`Reservation`Uygulanabilmesini sağlayan SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="dd248-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd248-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="dd248-117">-AppliedScopeType</span></span>
<span data-ttu-id="dd248-118">Güncelleştirilecek olan tür `Reservation`</span><span class="sxs-lookup"><span data-stu-id="dd248-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd248-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd248-119">-DefaultProfile</span></span>
<span data-ttu-id="dd248-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd248-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd248-121">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="dd248-121">-Reservation</span></span>
<span data-ttu-id="dd248-122">İçin yöneltme nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="dd248-122">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd248-123">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="dd248-123">-ReservationId</span></span>
<span data-ttu-id="dd248-124">`Reservation`Güncelleştirilecek</span><span class="sxs-lookup"><span data-stu-id="dd248-124">Id of the `Reservation` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd248-125">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="dd248-125">-ReservationOrderId</span></span>
<span data-ttu-id="dd248-126">`ReservationOrder`Güncelleştirilecek</span><span class="sxs-lookup"><span data-stu-id="dd248-126">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd248-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd248-127">-Confirm</span></span>
<span data-ttu-id="dd248-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd248-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd248-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd248-129">-WhatIf</span></span>
<span data-ttu-id="dd248-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd248-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd248-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd248-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd248-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd248-132">CommonParameters</span></span>
<span data-ttu-id="dd248-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd248-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd248-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd248-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd248-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd248-135">INPUTS</span></span>

### <span data-ttu-id="dd248-136">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="dd248-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="dd248-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd248-137">OUTPUTS</span></span>

### <span data-ttu-id="dd248-138">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="dd248-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="dd248-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd248-139">NOTES</span></span>

## <span data-ttu-id="dd248-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd248-140">RELATED LINKS</span></span>

