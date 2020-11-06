---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587102"
---
# <span data-ttu-id="a5683-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a5683-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="a5683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5683-102">SYNOPSIS</span></span>
<span data-ttu-id="a5683-103">Yerel Traffic Manager profil nesnesinden beklenen durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a5683-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5683-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5683-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5683-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5683-105">DESCRIPTION</span></span>
<span data-ttu-id="a5683-106">**Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet 'i yerel bir Azure Traffic Manager profili nesnesinden beklenen bir durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a5683-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="a5683-107">New-AzureRmTrafficManagerProfile veya Get-AzureRmTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5683-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="a5683-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="a5683-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="a5683-109">Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="a5683-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="a5683-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5683-110">EXAMPLES</span></span>

### <span data-ttu-id="a5683-111">Örnek 1: profilden beklenen durum kodu aralığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a5683-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="a5683-112">İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="a5683-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="a5683-113">İkinci komut $TrafficManagerProfile uygulamasında depolanan profilden beklenen durum kodu aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a5683-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a5683-114">Son komutu, Traffic Manager 'daki profili $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5683-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="a5683-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5683-115">PARAMETERS</span></span>

### <span data-ttu-id="a5683-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5683-116">-DefaultProfile</span></span>
<span data-ttu-id="a5683-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5683-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5683-118">-Dk</span><span class="sxs-lookup"><span data-stu-id="a5683-118">-Min</span></span>
<span data-ttu-id="a5683-119">Kaldırılacak durum kodu aralığındaki en düşük değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5683-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="a5683-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5683-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="a5683-121">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5683-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a5683-122">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a5683-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a5683-123">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5683-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a5683-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5683-124">-Confirm</span></span>
<span data-ttu-id="a5683-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5683-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5683-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5683-126">-WhatIf</span></span>
<span data-ttu-id="a5683-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5683-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5683-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5683-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5683-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5683-129">CommonParameters</span></span>
<span data-ttu-id="a5683-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5683-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5683-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5683-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5683-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5683-132">INPUTS</span></span>

### <span data-ttu-id="a5683-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5683-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a5683-134">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="a5683-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="a5683-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5683-135">OUTPUTS</span></span>

### <span data-ttu-id="a5683-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5683-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a5683-137">Bu cmdlet değiştirilmiş bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5683-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="a5683-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5683-138">NOTES</span></span>

## <span data-ttu-id="a5683-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5683-139">RELATED LINKS</span></span>

[<span data-ttu-id="a5683-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a5683-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="a5683-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5683-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a5683-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5683-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
