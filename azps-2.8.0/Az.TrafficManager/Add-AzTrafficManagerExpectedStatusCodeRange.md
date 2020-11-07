---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: c2758304f0140f5737a01611b18acf1449d0bb77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933141"
---
# <span data-ttu-id="e7bb3-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="e7bb3-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="e7bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bb3-103">Yerel bir Traffic Manager profil nesnesine beklenen bir durum kodu aralığı ekler.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="e7bb3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7bb3-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7bb3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="e7bb3-106">**Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine bir dizi beklenen durum kodu ekler.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="e7bb3-107">New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="e7bb3-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="e7bb3-109">Set-AzTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="e7bb3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7bb3-110">EXAMPLES</span></span>

### <span data-ttu-id="e7bb3-111">Örnek 1: profile beklenen bir durum kodu aralığı ekleme</span><span class="sxs-lookup"><span data-stu-id="e7bb3-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="e7bb3-112">İlk komut **Get-AzTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="e7bb3-113">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="e7bb3-114">İkinci komut, $TrafficManagerProfile depolanan profile beklenen bir durum kodu aralığı ekler.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="e7bb3-115">Son komutu, Traffic Manager 'daki profili $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="e7bb3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7bb3-116">PARAMETERS</span></span>

### <span data-ttu-id="e7bb3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7bb3-117">-DefaultProfile</span></span>
<span data-ttu-id="e7bb3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7bb3-119">-Max</span><span class="sxs-lookup"><span data-stu-id="e7bb3-119">-Max</span></span>
<span data-ttu-id="e7bb3-120">Eklenecek durum kodu aralığındaki en yüksek değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bb3-121">-Dk</span><span class="sxs-lookup"><span data-stu-id="e7bb3-121">-Min</span></span>
<span data-ttu-id="e7bb3-122">Eklenecek durum kodu aralığındaki en düşük değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bb3-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7bb3-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="e7bb3-124">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="e7bb3-125">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e7bb3-126">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bb3-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7bb3-127">-Confirm</span></span>
<span data-ttu-id="e7bb3-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7bb3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7bb3-129">-WhatIf</span></span>
<span data-ttu-id="e7bb3-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7bb3-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7bb3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bb3-132">CommonParameters</span></span>
<span data-ttu-id="e7bb3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7bb3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bb3-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7bb3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bb3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7bb3-135">INPUTS</span></span>

### <span data-ttu-id="e7bb3-136">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7bb3-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e7bb3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7bb3-137">OUTPUTS</span></span>

### <span data-ttu-id="e7bb3-138">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7bb3-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e7bb3-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7bb3-139">NOTES</span></span>

## <span data-ttu-id="e7bb3-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7bb3-140">RELATED LINKS</span></span>

[<span data-ttu-id="e7bb3-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="e7bb3-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="e7bb3-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7bb3-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e7bb3-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7bb3-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
