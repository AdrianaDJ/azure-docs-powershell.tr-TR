---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098078"
---
# <span data-ttu-id="ceed1-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ceed1-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="ceed1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceed1-102">SYNOPSIS</span></span>
<span data-ttu-id="ceed1-103">Yerel Traffic Manager profil nesnesinden beklenen durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ceed1-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="ceed1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ceed1-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceed1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ceed1-105">DESCRIPTION</span></span>
<span data-ttu-id="ceed1-106">**Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet 'i yerel bir Azure Traffic Manager profili nesnesinden beklenen bir durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ceed1-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ceed1-107">New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceed1-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="ceed1-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="ceed1-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ceed1-109">Set-AzTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="ceed1-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="ceed1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ceed1-110">EXAMPLES</span></span>

### <span data-ttu-id="ceed1-111">Örnek 1: profilden beklenen durum kodu aralığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ceed1-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ceed1-112">İlk komut **Get-AzTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="ceed1-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ceed1-113">İkinci komut $TrafficManagerProfile uygulamasında depolanan profilden beklenen durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ceed1-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ceed1-114">Son komutu, Traffic Manager 'daki profili $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ceed1-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ceed1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ceed1-115">PARAMETERS</span></span>

### <span data-ttu-id="ceed1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceed1-116">-DefaultProfile</span></span>
<span data-ttu-id="ceed1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ceed1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceed1-118">-Dk</span><span class="sxs-lookup"><span data-stu-id="ceed1-118">-Min</span></span>
<span data-ttu-id="ceed1-119">Kaldırılacak durum kodu aralığındaki en düşük değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="ceed1-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="ceed1-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ceed1-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="ceed1-121">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ceed1-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ceed1-122">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ceed1-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ceed1-123">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ceed1-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ceed1-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="ceed1-124">-Confirm</span></span>
<span data-ttu-id="ceed1-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ceed1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceed1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceed1-126">-WhatIf</span></span>
<span data-ttu-id="ceed1-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ceed1-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ceed1-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ceed1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceed1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceed1-129">CommonParameters</span></span>
<span data-ttu-id="ceed1-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ceed1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceed1-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceed1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceed1-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ceed1-132">INPUTS</span></span>

### <span data-ttu-id="ceed1-133">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ceed1-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ceed1-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ceed1-134">OUTPUTS</span></span>

### <span data-ttu-id="ceed1-135">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ceed1-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ceed1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ceed1-136">NOTES</span></span>

## <span data-ttu-id="ceed1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ceed1-137">RELATED LINKS</span></span>

[<span data-ttu-id="ceed1-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ceed1-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="ceed1-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ceed1-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ceed1-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ceed1-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
