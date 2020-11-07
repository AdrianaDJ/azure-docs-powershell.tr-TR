---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8f26030f726d472024dd788abb02e55f8eac4c6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934370"
---
# <span data-ttu-id="4f8c8-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="4f8c8-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="4f8c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8c8-103">Yerel Traffic Manager profil nesnesinden beklenen durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="4f8c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f8c8-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f8c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="4f8c8-106">**Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet 'i yerel bir Azure Traffic Manager profili nesnesinden beklenen bir durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="4f8c8-107">New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="4f8c8-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="4f8c8-109">Set-AzTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="4f8c8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f8c8-110">EXAMPLES</span></span>

### <span data-ttu-id="4f8c8-111">Örnek 1: profilden beklenen durum kodu aralığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4f8c8-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="4f8c8-112">İlk komut **Get-AzTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="4f8c8-113">İkinci komut $TrafficManagerProfile uygulamasında depolanan profilden beklenen durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="4f8c8-114">Son komutu, Traffic Manager 'daki profili $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="4f8c8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f8c8-115">PARAMETERS</span></span>

### <span data-ttu-id="4f8c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8c8-116">-DefaultProfile</span></span>
<span data-ttu-id="4f8c8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f8c8-118">-Dk</span><span class="sxs-lookup"><span data-stu-id="4f8c8-118">-Min</span></span>
<span data-ttu-id="4f8c8-119">Kaldırılacak durum kodu aralığındaki en düşük değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="4f8c8-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4f8c8-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="4f8c8-121">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="4f8c8-122">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="4f8c8-123">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4f8c8-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f8c8-124">-Confirm</span></span>
<span data-ttu-id="4f8c8-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8c8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f8c8-126">-WhatIf</span></span>
<span data-ttu-id="4f8c8-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f8c8-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8c8-129">CommonParameters</span></span>
<span data-ttu-id="4f8c8-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f8c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8c8-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f8c8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8c8-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f8c8-132">INPUTS</span></span>

### <span data-ttu-id="4f8c8-133">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4f8c8-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4f8c8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f8c8-134">OUTPUTS</span></span>

### <span data-ttu-id="4f8c8-135">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4f8c8-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4f8c8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f8c8-136">NOTES</span></span>

## <span data-ttu-id="4f8c8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f8c8-137">RELATED LINKS</span></span>

[<span data-ttu-id="4f8c8-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="4f8c8-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="4f8c8-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4f8c8-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4f8c8-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4f8c8-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
